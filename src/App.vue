<template>
  <div>
  <Header :esta_logado="true"/>
  <Primecomponent />
  <p class="paragrafo-pai">o dado de app é: {{testando}}</p>
  <LifeCycle />
  <Person />
</div>
</template>
<script>
  import Header from './components/Header.vue'
  import Primecomponent from './components/Primecomponent.vue'
  import LifeCycle from './components/LifeCycle.vue'
  import Person from './components/Person.vue'
  export default{
    name: 'App',
    components:{
      Header,
      Primecomponent,
      LifeCycle,
      Person
    },       
    data(){
      return{
        testando:"Teste"
      }       
    }       
  }       
</script>
<style>
  body{
    background-color: #333;
    color: #FFF;
  }
  a{color: red;}

  .teste{
    background-color: #000;
  }
</style>