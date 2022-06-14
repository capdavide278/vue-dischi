<template>
    <div>
        <select name="Seleziona genere" id="musica" @change = "$emit('selection', userText)" v-model="userText">
            <option value="all">Tutti</option>
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Metal">Metal</option>
            <option value="Jazz">Jazz</option>
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
select{
    margin-top: 25px;
    margin-left: 13%;
}
</style>