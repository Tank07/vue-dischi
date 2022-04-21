<template>
  <div class=" text-center my-5">
      
      <img :src="poster" alt="" class="img-fluid">
      <h3 class="text-white my-3">{{title}} </h3>
      <h6 class="my-3"> {{author}} </h6>
      <h6 class="text-muted my-3"> {{year}} </h6>
      <h6 class="d-none my-3"> {{genre}} </h6>
    
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
      genre: String
  }
}
</script>


<style scoped>

div{
  background-color: #2e3a46;
}


</style>