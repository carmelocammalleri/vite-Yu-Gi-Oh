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

   }
  }
</script>

<template>

  <main class="mainContainer container"> 

      <!-- section card -->
    <div class="sectionCard">
      <span class="finder d-block">ho trovato 5 carte</span>
      <div class="counterCard d-flex flex-wrap justify-content-between">
        <cardSection v-for="card in store.cardsList" 
        :key="card.id" 
        :nameObj="card.name" 
        :imageObj="card.card_images[0].image_url"
        :typeObj="card.archetype"/>
      </div>
    </div>

  </main>
</template>

<style>

</style>