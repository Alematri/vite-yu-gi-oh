<script>
  import axios from 'axios';
  import {store} from './data/store.js';
  import Header from './components/Header.vue';
  import CardsContainer from './components/CardsContainer.vue';
  import SearchBar from './components/partials/SearchBar.vue';
  import Loader from './components/partials/Loader.vue';

  export default{

  name: 'App',

  components:{
    Header,
    CardsContainer,
    SearchBar,
    Loader
  },
  data(){
    return{
      store
    }
  },

  methods:{
    getApi(){
      store.isLoading= true;
      axios.get(store.apiUrl,{
        params: {
          num: 1000,
          offset: 0,
          archetype: store.archetypeToSearch
        }
      })
      .then(res =>{
        store.cardList = res.data.data;
        store.isLoading = false;
        store.cardList.forEach( card => {
          if(!store.archetypeList.includes(card.archetype)){
            store.archetypeList.push(card.archetype)
          }
        })
      })
      .catch(err =>{
        console.log(err);
        store.isLoading = false;
      })
    }
  },

  mounted(){
    this.getApi();
  }
}


</script>

<template>
  <Header titleStr="Yu-Gi-Oh Api"/>
  <SearchBar @startSearch="getApi"/>
  <Loader v-if="store.isLoading"/>
  <CardsContainer v-else/>
</template>

<style lang="scss">

  @use './scss/main.scss';

</style>