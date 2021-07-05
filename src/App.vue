<template>
  <div id="app"> 
    <app-header></app-header>
    <app-home></app-home>
  </div>
</template>

<script>
import Header from './components/Header'
import Home from './components/Home'

export default {
  name: 'App',
  components: {
    'app-header': Header,
    'app-home': Home
  },

  data(){
    return {
    }
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;

}
</style>
