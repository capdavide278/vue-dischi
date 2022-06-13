<template>
    <div>
        <select name="Seleziona genere" id="musica" @click.prevent = "$emit('SelezionaGenere', userText)" v-model="userText">
            <option value="all">Tutti</option>
            <option value="rock">Rock</option>
            <option value="pop">Pop</option>
            <option value="metal">Metal</option>
            <option value="jazz">Jazz</option>
        </select>
    </div>
</template>

<script>
export default {
  name: 'RicercaMusica',
  data(){
    return{
        userText : "",
    }
  },

  methods: {

  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>