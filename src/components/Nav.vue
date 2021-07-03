<template>
  <div>
    <h1 class="text-center">Header {{msg}}</h1>  
  </div>  
</template>

<script>

export default {
  data(){
    return {
      
    }
  },
  props: {
    msg: String
  }
}
</script>

<style scoped>
  div {
    background: black;
    color: white;
  }

</style>