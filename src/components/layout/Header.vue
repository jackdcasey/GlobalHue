<template>
    <div class="wrapper">
        <nav class="navbar">
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
  color: #ffffff;

  background: rgb(12,0,214);
  background: linear-gradient(to right, rgba(12,0,214,1) 0%, rgba(0,161,255,1) 100%);

  position: sticky;
  top: 0;
}

span:first-of-type {
    flex: 1;
}

</style>