<script>
  import axios from 'axios';
  import {store} from './data/store.js';
  import Header from './components/Header.vue';
  import CardsContainer from './components/CardsContainer.vue';

  export default{

  name: 'App',

  components:{
    Header,
    CardsContainer
  },
  data(){
    return{
      store
    }
  },

  methods:{
    getApi(){
      axios.get(store.apiUrl)
      .then(res =>{
        store.cardList = res.data.data;
      })
      .catch(err =>{
        console.log(err);
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
  <CardsContainer />
</template>

<style lang="scss">

  @use './scss/main.scss';

</style>