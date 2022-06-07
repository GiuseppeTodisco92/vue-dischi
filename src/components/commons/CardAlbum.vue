<template>
  <div class="album__card">
      <img :src="album.poster" :alt="album.title">
      <h3>{{album.title}}</h3>
      <p>{{album.author}}</p>
      <p>{{album.year}}</p>
  </div>
</template>

<script>
export default {
    name:"CardAlbum",
    props: {
        album: Object,
    }
}
</script>

<style lang="scss" scoped>
.album__card{
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 300px;
    margin: .625rem;
    background-color: var(--primary-color);

    h3{
        font-weight: bold;
        font-size: 1.75rem;
        text-transform: uppercase;
        padding-bottom: 1.5625rem;
    }
    img{
        width: 200px;
        padding: 20px;
    }
    p{
        line-height: 5px;
        color: gray;
        font-size: small;
    }
}
</style>
