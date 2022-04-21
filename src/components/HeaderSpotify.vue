<template>
  <div>
    <img src="../assets/spotify-logo.png" alt="">
    <select name="genre" id="genre">
      <option value="null">Null</option>
      <option value="rock">Rock</option>
      <option value="pop">Pop</option>
      <option value="jazz">Jazz</option>
      <option value="metal">Metal</option>
  </select>
  </div>
</template>

<script>
export default {
  name: 'HeaderSpotify',
}
</script>


<style scoped>

div{
    background-color: #2e3a46;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

img{
  
    height: 60px;
    width: auto;
}
</style>