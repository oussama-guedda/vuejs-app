<template>
  <div>
    <ul v-for="car in cars" :key="car.name">
    <label> Name: <input type="texte" v-model="car.name"/></label>
    <label> modele: <input type="texte" v-model="car.modele"/></label>
    <label> year: <input type="texte" v-model="car.year"/></label><br>
      <li>{{ car.name }}</li>
      <li>{{ car.modele }}</li>
      <li>{{ car.year }}</li>
    </ul>
    <button @click="addcar">Add car</button>
    <p>Nombre de car : {{ counter }}</p>
  </div>
</template>
<script>
export default {
  props: ['name', 'modele', 'year'],
  data() {
    return {
      cars: []
    };
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
  mounted: {}
};
</script>
<style scoped>
</style>