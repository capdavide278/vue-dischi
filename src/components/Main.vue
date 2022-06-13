<template>
    <main>
        <RicercaMusica @selection="changeAlbum"/>
        <div id="background_copertine">
            <DiscCard
            v-for="(item, index) in filteredAlbum" :key="index"
            :discDescription="item"
          />
        </div>
    </main>
</template>

<script>
import axios from "axios"
import DiscCard from "./DiscCard.vue";
import RicercaMusica from "./RicercaMusica.vue";

export default {
    name: "myMain",
    components: { 
        DiscCard,
        RicercaMusica 
    },
    data() {
        return {
            apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
            album: [],
            selezionato : ''
        };
    },
    created() {
        axios.get(this.apiUrl)
            .then(result => {
            this.album = result.data.response;
            console.log(result);
        })
            .catch(error => {
            console.log("Errore", error);
        });
    },
    computed : {
        filteredAlbum(){
            if(this.selezionato === 'all'){
                return this.album
            }
            return this.album.filter((item) => {
                return item.genre.includes(this.selezionato)
            })
        }
    },

    methods: {
        changeAlbum(selezione){
            this.selezionato = selezione;
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
main{
    background-color: #1e2d3b;
    height: 100vh;
}

#background_copertine{
  display: flex;
  flex-wrap: wrap;
  width: 80%;
  margin: auto;
}

</style>
 