<template>
  <div>
      <form action="">

        <select name="genre" id="genre"
                v-model="searchGenere" 
                @click.prevent="$emit( 'funzioneRicerca', searchGenere )">

            <option value="">Choose a genre</option>
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
            <option value="Metal">Metal</option>
        </select>
          
      </form>
  </div>            
       
</template>

<script>
export default {
  name: 'RicercaGenre',
  data(){
    return{
      searchGenere: ''
    }
  }
}   
</script>


<style scoped>



</style>