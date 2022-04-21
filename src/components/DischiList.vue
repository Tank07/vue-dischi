<template>
<div class="container">

  <div class="row row-cols-5 ">
    <DischiProps
    v-for="(element, index) in dischiArray"
    :key ="index"
    :poster = "element.poster"
    :title = "element.title"
    :author = "element.author"
    :year =  "element.year"
    />
  </div>

</div>
</template>

<script>

import axios from 'axios';

import DischiProps from "./DischiProps.vue"


export default {
  name: 'DischiList',
  components:{
    DischiProps
      
  },
  data(){
      return{
          dischiArray:[]
      }
  },
  created(){
      axios.get("https://flynn.boolean.careers/exercises/api/array/music")
            .then( (res) => {
              console.log(res.data.response);
              this.dischiArray = res.data.response
            }
             )
  }
}

</script>

<style >



</style>
