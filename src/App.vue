<template>
  <div class="wrap">
    <div id="app">
      <Header />
      <CitiesList />
    </div>
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
html,
body {
    height: 100%;
}

.wrap {
background: rgb(9,0,162);
background: linear-gradient(90deg, rgba(12,0,214,0.4) 0%, rgba(0,212,255,0.4) 100%);
  width: 100%;
  height: 100%;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
