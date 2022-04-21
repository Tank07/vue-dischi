<template>
  <div>
    
        <select form="myGenre" name="genre" id="genre"
        v-model="searchGenere">
            <option value="">Choose a genre</option>
            <option value="rock">Rock</option>
            <option value="pop">Pop</option>
            <option value="jazz">Jazz</option>
            <option value="metal">Metal</option>
        </select>
         <form id="myGenre">
            <input type="submit" @click.prevent="$emit( 'funzioneRicerca', searchGenere )">
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