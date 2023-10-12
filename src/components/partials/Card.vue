<script>
export default{
  name: 'Card',
  props:{
    name: String,
    archetype: String,
  }
}
</script>

<template>
  <div class="col-2">
    <div class="sc-card">
      <img src="https://images.ygoprodeck.com/images/cards/64163367.jpg">
      <div class="card-text">
        <h4>{{name}}</h4>
        <p>{{archetype}}</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.col-2{
  .sc-card{
    text-align: center;
    img{
      max-width: 100%;
    }
    .card-text{
      background-color: orange;
      height: 150px;
      h4{
        color: white;
        padding: 3px;
      }
    }
  }
}
</style>