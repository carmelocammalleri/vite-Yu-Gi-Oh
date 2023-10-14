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
  <nav class="container">
    <select v-model="store.archetypeToSearch" class="archetype my-3" name="Archetype">
      <option selected value="">Select</option>
      <option 
        v-for="(cardtype, index) in store.archetypeList"
        :key="index" 
        :value="cardtype.archetype_name"> {{cardtype.archetype_name}} </option>
      </select>
      <button @click="$('searchArchetype')">Cerca</button>
  </nav>
</template>
  


