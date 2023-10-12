<script>
  import cardSection from './partials/CardSection.vue';
  import { store } from '../data/store';

  export default{
    name: 'Main',
    components:{
      cardSection
    },
    data(){
      return{
        store
      }
    },
    mounted(){
    console.log(store.cardsList);
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