<template>
  <div>
    <h1>Countries</h1>
    <select @change="onChange()" v-model="selected">
      <option value="0">Select Country</option>
      <option :key="id" v-for="(country,id) in countries">{{country.Country}}</option>
    </select>
  </div>
</template>

<script>


export default {

  name: 'DataBoxes',
  props: ['countries'],
  data(){
    return {
      selected: 0
    }
  },
  methods: {
    onChange(){

      let country = this.countries.find((item) => item.ID === this.selected);
      console.log(country)
      console.log(this.selected);
      this.$emit('country-data', country);
    }
  }

}
</script>

