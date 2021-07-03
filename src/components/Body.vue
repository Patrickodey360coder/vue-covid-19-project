<template>
  <div>
    <input type="text" v-model="todoItem">
    <button>Add</button>
    <ul>
      <li :key="todo" v-for="todo in todos">{{todo}}</li>
    </ul>
  <h1>Nigerian Skateboarders</h1> 
   <div @click="del" class="skaters" :key="skater.id" v-for="skater in skaters">
     <p><b>NAME:</b>{{skater.name}}</p>
     <p><b>STANCE:</b>{{skater.stance}}</p>
     <p><b>SPONSORS:</b>{{skater.sponsor}}</p>
   </div>
  </div>  
</template>

<script>

export default {
  data(){
    return {
      todos: [],
      todoItem: '',
      count: 0
    }
  },
  props: {
    skaters: Array
  },
  methods: {
    del(){

    }
  }
}
</script>

<style scoped>
.skaters {
  border: 1px solid red;
}

</style>