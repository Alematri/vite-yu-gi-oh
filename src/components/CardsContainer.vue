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
  }
}
</script>

<template>

  <div class="container">
    <div class="row">
      <div class="col founded">Found 39 card</div>
    </div>
    <div class="row">
      <Card
        v-for="card in store.cardList"
        :key="card.id"
        :name="card.name"
        :archetype="card.archetype"
        :image="card.card_images[0].image_url"
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
        border-right: 12px solid white;
        border-left: 12px solid white;
      }
    }
  }
</style>
