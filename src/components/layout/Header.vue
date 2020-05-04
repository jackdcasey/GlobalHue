<template>
    <div class="wrapper">
        <nav class="navbar navbar-fixed-top navbar-dark bg-dark">
        <a class="navbar-brand">GlobalHue</a>
        <span class="navbar-text">See the color of the sky, from around the world!</span>
        <a class="github-button" href="https://github.com/jackdcasey/globalhue" data-icon="octicon-star" data-size="large" data-show-count="true" aria-label="Star jackdcasey/globalhue on GitHub">Star</a>        </nav>
    </div>
</template>

<script>
export default {
    name: 'Header',
    mounted() {
      let githubButtonScript = document.createElement('script')
      githubButtonScript.setAttribute('src', 'https://buttons.github.io/buttons.js')
      document.head.appendChild(githubButtonScript)
    },
}
</script>

<style>

.wrapper {
  position: sticky;
  top: 0;
}

span:first-of-type {
    flex: 1;
}

</style>