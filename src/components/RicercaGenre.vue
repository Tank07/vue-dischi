<template>
  <div>
      <form action="">

        <select name="genre" id="genre"
                v-model="searchGenere" 
                @click.prevent="$emit( 'funzioneRicerca', searchGenere )">

            <option value="">Choose a genre</option>
            <option value="rock">Rock</option>
            <option value="pop">Pop</option>
            <option value="jazz">Jazz</option>
            <option value="metal">Metal</option>
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