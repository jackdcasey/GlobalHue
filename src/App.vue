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
  background: rgb(64,64,64);
  background: linear-gradient(90deg, rgba(64,64,64,1) 0%, rgba(135,135,135,1) 100%);

  width: 100%;
  height: 100%;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
