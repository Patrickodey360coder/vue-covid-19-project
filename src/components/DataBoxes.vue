<template>
  <div>
    <h1>Cases</h1>
    <p>Total cases: {{stats.TotalConfirmed.toLocaleString()}}</p>
    <p>Total Deaths: {{stats.TotalDeaths.toLocaleString()}}</p>
    <p>Total Recovered: {{stats.TotalRecovered.toLocaleString()}}</p>
    <p>New Confirmed: {{stats.NewConfirmed.toLocaleString()}}</p>
    <p>New Deaths: {{stats.NewDeaths.toLocaleString()}}</p>
    <p>New Recovered: {{stats.NewRecovered.toLocaleString()}}</p>

 


  </div>
</template>

<script>


export default {

  name: 'DataBoxes',
  props: ['stats'],

}
</script>

