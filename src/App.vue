<template>
  <div id="app">
    <Header />
    <CitiesList />

  </div>
</template>

<script>
import Header from './components/layout/Header'
import CitiesList from './components/CitiesList'

export default {
  name: 'App',
  components: {
    Header,
    CitiesList
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
