<script>

import {store} from '../data/store';
import Card from './partials/Card.vue'

export default{
  name: 'CardsContainer',
  components:{
    Card
  },
  data(){
    return{
      store
    }
  },
  mounted(){
    console.log(store.cardList);
  }
}
</script>

<template>

  <div class="container my-5">
    <div class="row">
      <div class="col founded">Found 39 card</div>
    </div>
    <div class="row">
      <Card
        v-for="data in store.cardList"
        :key="data.id"
        :name="data.name"
        :archetype="data.archetype"
      />
    </div>
  </div>

</template>

<style lang="scss" scoped>
  .container{
    background-color: white;
    padding: 30px;
    .row{
      .founded{
        background-color: black;
        color: white;
        line-height: 40px;
      }
    }
  }
</style>
