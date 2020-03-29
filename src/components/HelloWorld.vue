<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Hello {{ person.firstName }} {{ person.lastName }} de {{ from }}</h2>
    {{ message }} <br>  <br>  
    <label> FirstName: <input type="texte" v-model="person.firstName"/></label>
    <label> LastName: <input type="texte" v-model="person.lastName"/></label>
    <label> message: <input type="texte" v-model="message"/></label><br>
    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    message: String
  },
  data(){
    return {
      person: {
        firstName : "oussama",
        lastName : "guedda"
      },
      from : "Tunisie"
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
