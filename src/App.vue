<script>
  import Header from './components/Header.vue';
  import Main from './components/Main.vue';
  import SearchBar from './components/partials/SearchBar.vue';
  import { store } from './data/store';
  import axios from 'axios';

  export default {
      name: 'App',
      components: {
        Header,
        Main,
        SearchBar
      },
      Data(){
        return{
          store
        }
      },
      methods: {
        getApi(){
          axios.get(store.apiUrl)
          .then( risultato =>{
            store.cardsList = risultato.data.data;
            // console.log(risultato.data.data);
          })
        },
        getArchtype(){
          axios.get(store.apiUrlArchetype)
          .then( res =>{
          store.archetypeList = res.data;
          })
        }
      },
      mounted(){
        this.getApi();
        this.getArchtype()
    }
  }
</script>

<template>
  <Header/>
  <SearchBar @searchArchetype="getArchtype"/>
  <Main/>
</template>

<style lang="scss">
  @use './scss/main.scss';
</style>
