<template>
  <div>
    <h1>{{text}}</h1>
    <h1>{{timestamp}}</h1>
  </div>
</template>

<script>
import moment from "moment"  

export default {

  name: 'DataTile',
  props: ['text', 'dataDate'],
  computed: {
    timestamp: function(){
      return moment(this.dataDate).format("MMMM Do YYYY, h:m:s")
    }
  }
}
</script>

