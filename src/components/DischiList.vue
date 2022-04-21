<template>
<div class="container">

   <RicercaGenre @funzioneRicerca="metodoSearch"/>

  <div class="row row-cols-5 ">
    <DischiProps
    v-for="(element, index) in filtroGenere()"
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
          testoGenere: ''
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
      this.testoGenere = testo
      console.log(this.testoGenere)
    },
    filtroGenere(){
      if( this.testoGenere === '' ){
        return this.dischiArray
      } else{
        return this.dischiArray.filter( (element) => {
          return element.genre.includes(this.testoGenere)
        } )
      }
    }
  }
}

</script>

<style >



</style>
