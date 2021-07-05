<template>
  <div class="container mx-auto">
    <div v-if="!loading">
      <data-title :text="title" :dataDate="dataDate"></data-title>
      <data-boxes :stats="stats"></data-boxes>
      <country-data @country-data="getCountrydata" :countries="countries"></country-data>
    </div>

    <div v-else>
      <h1>loading</h1>
    </div>
  </div>
</template>

<script>
import DataTitle from './DataTitle'
import DataBoxes from './DataBoxes';
import CountryData from './CountryData'


export default {
  name: 'Home',
  components: {
    'data-title':   DataTitle,
    'data-boxes':   DataBoxes,
    'country-data': CountryData
  },
  data() {
    return {
      loading: true,
      dataDate: '',
      title: 'Global',
      loadingGif: '',
      countries: [],
      stats: []

    }
  },
  methods: {
    async fetchCovid(){
      const res = await fetch('https://api.covid19api.com/summary');
      const data = await res.json();
      return data;
    },

    getCountrydata(country){
      this.stats = country
      this.Global = country.Country
    }
  },

  async created(){
    const data = await this.fetchCovid();
    console.log(data)

    this.dataDate = data.Date
    this.stats = data.Global
    this.countries = data.Countries
    this.loading = false

  },

}
</script>

