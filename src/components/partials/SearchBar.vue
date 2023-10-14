<script>

  import {store} from '../../data/store';

  export default{
  name: 'SearchBar',
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
      <div class="col-2 mt-4 mb-4">
        <select @click="$emit('startSearch')" v-model="store.archetypeToSearch" class="form-select">
          <option value="blue-eyes">Blue-Eyes</option>
          <option value="abc">ABC</option>
          <option value="alien">Alien</option>
          <option value="Materiactor">Materiactor</option>
        </select>
      </div>
    </div>
  </div>

</template>

<style lang="scss" scoped>

</style>