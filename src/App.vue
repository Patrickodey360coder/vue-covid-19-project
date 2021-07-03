<template>
  <div id="app"> 
    <Nav/>
    <Body :skaters="skaters"/>
  </div>
</template>

<script>
import Nav from './components/Nav.vue'
import Body from './components/Body.vue'

export default {
  name: 'App',
  components: {
    Nav,
    Body,
  },

  data(){
    return {
      skaters: [
        {id:1, name: 'Patrick', stance: 'Goofy', sponsor: 'NikeSb'},
        {id:2, name: 'Lukman', stance: 'Regular', sponsor: 'Spit Fire'},
        {id:3, name: 'Alirang', stance: 'Goofy', sponsor: 'Vans'},
        {id:4, name: 'Mahmmud', stance: 'Regular', sponsor: 'Etnies'}
      ]
    }
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
