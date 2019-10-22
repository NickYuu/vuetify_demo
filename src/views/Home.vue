<template>
  <div class="home">
    <carousel class="carousel"/>
  </div>
</template>

<script>
  import Carousel from "@/components/carousel/Carousel"
  export default {
    name: 'home',
    components: {
      Carousel
    }
  }
</script>

<style scoped>
  .carousel {
    margin-top: 10px;
  }
</style>