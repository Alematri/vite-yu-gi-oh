<script>
  export default{
  name: 'Header',
  props:{
    titleStr: String
  }
}
</script>

<template>
  <header class="ps-2">
    <div class="title">
      <img src="/yugioh-logo.png">
      <h1>{{titleStr}}</h1>
    </div>
  </header>
</template>

<style lang="scss" scoped>
  header{
    background-color: white;
    height: 80px;
    .title{
      height: 100%;
      align-items: center;
      display: flex;
      img{
        height: 25px;
        width: 80px;
        margin-right: 20px;
      }
      h1{
        font-size: 50px;
      }
    }

  }
</style>
