<script>
  import cardSection from './partials/CardSection.vue';
  import searchBar from './partials/SearchBar.vue';
  import { store } from '../data/store';

  export default{
    name: 'Main',
    components:{
      cardSection,
      searchBar
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

    <searchBar/>

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