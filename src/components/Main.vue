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
    <select class="archetype my-3" name="Archetype" id="">
      <option value="alien"> alien</option>
      <option value="aliens"> aliens</option>
      <option value="aliend"> aliend</option>
      <option value="alienf"> alienf</option>
    </select>
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