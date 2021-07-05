<template>
  <div class="container mx-auto">
    <div v-if="!loading">
      <data-title :text="title" :dataDate="dataDate"></data-title>
    </div>

    <div v-else>
      <h1>loading</h1>
    </div>
  </div>
</template>

<script>
import DataTitle from './DataTitle'


export default {
  name: 'Home',
  components: {
    'data-title': DataTitle,
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
    }
  },

  async created(){
    const data = await this.fetchCovid();
    console.log(data)

    this.dataDate = data.Date
    this.stats = data.Global
    this.countries = data.countries
    this.loading = false

  },

}
</script>

