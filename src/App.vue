<script>
  import './components/Header.vue'
  import './components/Main.vue'

  export default {
    name: 'App',
    components: {
      Header,
      Main
    }
  }
</script>

<template>
  <Header/>
  <Main/>
</template>

<style lang="scss">
  @use './scss/main.scss';
</style>
