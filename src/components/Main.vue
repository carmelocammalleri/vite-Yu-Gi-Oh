<script>
  import cardSection from './partials/CardSection.vue'
  export default{
    name: 'Main',
    components:{
      cardSection
    }
  }
</script>

<template>

  <main class="mainContainer container"> 
    <div class="counterCard">
      <span class="finder d-block">ho trovato 5 carte</span>
      <cardSection/>
    </div>

  </main>
</template>

<style>

</style>