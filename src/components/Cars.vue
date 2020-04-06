<template>
  <div>
    <ul v-for="car in cars" :key="car.name">
      <label>
        Name:
        <input type="texte" v-model="car.name" />
      </label>
      <label>
        modele:
        <input type="texte" v-model="car.modele" />
      </label>
      <label>
        year:
        <input type="texte" v-model="car.year" />
      </label>
      <br />
      <li>{{ car.name }}</li>
      <li>{{ car.modele }}</li>
      <li>{{ car.year }}</li>
    </ul>
    <button @click="addcar">Add car</button>
    <p>Nombre de car : {{ counter }}</p>
  </div>
</template>

<script>
import Vue from "vue";
import VueResource from "vue-resource";
Vue.use(VueResource);

export default {
  props: ["name", "modele", "year"],
  data() {
    return {
      cars: []
    };
  },
  http: {
    root: "http://localhost:3000"
  },
  methods: {
    addcar() {
      this.cars.push({
        name: this.name,
        modele: this.modele,
        year: this.year
      });
    }
  },
  computed: {
    counter() {
      return this.cars.length;
    }
  },
  mounted() {
    this.$resource("cars")
      .get()
      .then(
        response => {
          this.cars = response.data
        },
        response => {
          console.log('erreur',response)
        }
      );
  }
};
</script>

<style scoped>
</style>