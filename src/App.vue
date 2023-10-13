<script>
  import Header from './components/Header.vue';
  import Main from './components/Main.vue';
  import { store } from './data/store';
  import axios from 'axios';

  export default {
      name: 'App',
      components: {
        Header,
        Main
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
          })
          .catch( error =>{
            console.log(error.data.data)
          })
        }
      },
    mounted(){
      this.getApi();
    }
  }
</script>

<template>
  <Header/>
  <Main/>
</template>

<style lang="scss">
  @use './scss/main.scss';
</style>
