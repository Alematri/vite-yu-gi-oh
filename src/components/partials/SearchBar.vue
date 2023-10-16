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
    <div class="row align-items-center">
      <div class="col-3">
        <h4>Select an archetype:</h4>
      </div>
      <div class="col-2 mt-4 mb-4">
        <select @change="$emit('startSearch')" v-model="store.archetypeToSearch" class="form-select">
          <option
          v-for="(archetype, index) in store.archetypeList"
          :key="index"
          :value="archetype"
          >{{ archetype }}</option>
        </select>
      </div>
    </div>
  </div>

</template>

<style lang="scss" scoped>

</style>