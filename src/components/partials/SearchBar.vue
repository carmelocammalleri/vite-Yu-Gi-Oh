<script>
  import { store } from '../../data/store';

  export default {
    name: 'SearchBar',

    data(){
      return{
        store
      }
    }
  }
</script>

<template>

  <!-- select and button -->
  <select v-model="store.archetypeToSearch" class="archetype my-3" name="Archetype" id="">
    <option value="">Select</option>
    <option 
      v-for="card in store.cardsList" 
      :key="card.id" 
      :value="card.archetype"> {{card.archetype}} </option>
    </select>
    <button @click="$emit('startSearch')">search</button>
</template>
  


