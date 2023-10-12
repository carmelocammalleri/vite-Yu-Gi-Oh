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
      <h4>ho trovato 5 carte</h4>
      <cardSection/>
    </div>

  </main>
</template>

<style>

</style>