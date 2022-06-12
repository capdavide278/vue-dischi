<template>
    <header>
        <img src="../assets/Spotify_App_Logo.svg.png" alt="">
    </header>
</template>

<script>
export default {
  name: 'myHeader',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
header{
    background-color: #2e3a46;
    height: 80px;
    img{
        height: 80px;
        width: 80px;

    }
}

</style>
