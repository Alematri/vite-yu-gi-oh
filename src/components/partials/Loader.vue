<script>
  export default{
  name: 'Loader'
}
</script>

<template>
  <div class="text-center py-5">
    <span class="loader"></span>
  </div>
</template>

<style lang="scss" scoped>
.loader {
    width: 48px;
    height: 48px;
    border: 5px solid #FFF;
    border-bottom-color: #FF3D00;
    border-radius: 50%;
    display: inline-block;
    box-sizing: border-box;
    animation: rotation 1s linear infinite;
    }

    @keyframes rotation {
    0% {
        transform: rotate(0deg);
    }
    100% {
        transform: rotate(360deg);
    }
    } 
</style>