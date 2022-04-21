<template>
<div class="container">

   <RicercaGenre @funzioneRicerca="metodoSearch"/>

  <div class="row row-cols-5 ">
    <DischiProps
    v-for="(element, index) in filtraggio"
    :key ="index"
    :poster = "element.poster"
    :title = "element.title"
    :author = "element.author"
    :year =  "element.year"
    :genre = "element.genre"
    />
  </div>

</div>
</template>

<script>

import axios from 'axios';

import DischiProps from "./DischiProps.vue"
import RicercaGenre from "./RicercaGenre.vue"


export default {
  name: 'DischiList',
  components:{
    DischiProps,
    RicercaGenre
    
      
  },
  data(){
      return{
          dischiArray:[],
          testoRicerca: ''
      }
  },
  created(){
      axios.get("https://flynn.boolean.careers/exercises/api/array/music")
            .then( (res) => {
              console.log(res.data.response);
              this.dischiArray = res.data.response
            }
             )
  },
  methods: {
    metodoSearch( testo ){
      console.log(testo)
      this.testoRicerca = testo
      console.log(this.testoRicerca)
    },
    filtraggio(){
      if( this.testoRicerca === '' ){
        return this.dischiArray
      } else{
        return this.dischiArray.filter( (element) => {
          return element.genre.includes(this.testoRicerca)
        } )
      }
    }
  }
}

</script>

<style >



</style>
