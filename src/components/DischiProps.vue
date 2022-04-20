<template>
  <div class="col-3 text-center my-5">
      
      <img :src="poster" alt="">
      <h3 class="my-3">{{title}} </h3>
      <h6 class="my-3"> {{author}} </h6>
      <h6 class="text-muted my-3"> {{year}} </h6>
    
  </div>
</template>

<script>
export default {
  name: 'DischiProps',

  props: {
      poster: String,
      title: String,
      author: String,
      year: String,
  }
}
</script>


<style scoped>


</style>