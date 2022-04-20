<template>
  <div>
    
  </div>
</template>

<script>

import axios from 'axios';



export default {
  name: 'DischiList',
  components:{
      
  },
  data(){
      return{
          dischiArray:[]
      }
  },
  created(){
      axios.get("https://flynn.boolean.careers/exercises/api/array/music")
            .then( (res) => {
              console.log(res);
              
            }
             )
  }
}

</script>

<style >



</style>
