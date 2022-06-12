<template>
    <section>
        <div id="disco">
            <img :src="discDescription.poster" :alt="discDescription.title">
            <div id="info">
                <h2>{{discDescription.title}}</h2>
                <h4>{{discDescription.author}}</h4>
                <h4>{{discDescription.genre}}</h4>
                <h4>{{discDescription.year}}</h4>
            </div>
        </div>
    </section>
</template>

<script>
export default {
  name: 'DiscCard',
  props: {
    discDescription : Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#disco{
   /*  flex-basis: calc(100% / 5); */
    height: 80%;
    background-color: #2e3a46;
    margin: 50px;
    width: 200px;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
}

img{
    width: 170px;
    /* height: 200px; */
    padding: 20px 0;
}

h2{
    color:white;
    text-align: center;
    display: flex;
    flex-wrap: wrap;
}

h4{
    color: #495a6e;
    text-align: center;
}

</style>