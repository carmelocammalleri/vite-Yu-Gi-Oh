<script>
  import { store } from '../../data/store';
  import axios from 'axios';

  export default {
    name: 'SearchBar',

    data(){
      return{
        store
      }
    },
    methods:{
      getArchtype(){
        axios.get(store.apiUrlArchetype)
        .then(res =>{
          store.archetypeList = res.data;
        })
    }
    },
    mounted(){
      this.getArchtype()
    }
  }
</script>

<template>

  <!-- select and button -->
  <select v-model="store.archetypeToSearch" class="archetype my-3" name="Archetype" id="">
    <option selected value="">Select</option>
    <option 
      v-for="(cardtype, index) in store.archetypeList" 
      :key="index" 
      :value="cardtype.archetype_name"> {{cardtype.archetype_name}} </option>
    </select>
    <button @click="$emit('startSearch')">search</button>
</template>
  


