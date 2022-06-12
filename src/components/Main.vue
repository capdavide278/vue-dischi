<template>
    <main>
        <div id="background_copertine">

        </div>
    </main>
</template>

<script>
import axios from "axios"

export default {
  name: 'myMain',

  data(){
    return{
      apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
      copertine_album : []
    }
  },
  craeted(){
    axios.get(this.apiUrl)
    .then(result => {
      console.log(result)
    })
    .catch(error => {
      console.log("Errore", error);
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
main{
    background-color: #1e2d3b;
    height: 100vh;
}

</style>
 