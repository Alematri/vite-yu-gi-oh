<script>
  export default{
  name: 'Header',
  props:{
    titleStr: String

  }
}
</script>

<template>
  <header class="ps-2 py-2">
    <h1>{{titleStr}}</h1>
  </header>
</template>

<style lang="scss" scoped>
  header{
    background-color: white;
  }
</style>
