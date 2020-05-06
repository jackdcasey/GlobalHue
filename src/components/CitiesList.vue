<template>
    <div>
        <div v-for="city in cities" :key="city.city">
            <City v-bind:city=city />
        </div>
    </div>

</template>

<script>
import City from './City'
import axios from 'axios'

export default {
    name: 'CitiesList',
    data () {
        return {
            cities: null
        }
    },
    mounted() {
        axios
            .get('https://api.globalhue.xyz/cities/')
                .then(res => this.cities = res.data.Items)
                .then(() => this.cities.sort((a, b) => b.timedata.raw_offset - a.timedata.raw_offset))
                .catch(err => console.log(err))
    },
    components: {
        City
  }
}
</script>

<style>

</style>