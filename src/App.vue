<template>
  <div id="app">
    <HeaderSpotify/>
    <DischiList/>
  </div>
</template>

<script>

  import "bootstrap"

import HeaderSpotify from './components/HeaderSpotify.vue'
import DischiList from './components/DischiList.vue'

export default {
  name: 'App',
  components: {
    HeaderSpotify,
    DischiList
  }
}
</script>

<style lang="scss">

  @import "bootstrap/dist/css/bootstrap.min.css";

#app {
  
}
</style>
