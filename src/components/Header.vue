<template>
    <header>
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Spotify_logo_without_text.svg/768px-Spotify_logo_without_text.svg.png" alt="">
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
        height: 60px;
        width: 50px;
        padding-top: 15px;

    }
}

</style>
