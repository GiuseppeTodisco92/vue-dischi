<template>
  <section>
      <div class="container">
          <div class="row">
            <card-album class="col" v-for="(album,index) in albums" :key="index" :album="album"/>
            
           
          </div>
      </div>
  </section>
</template>

<script>
import axios from 'axios';
import CardAlbum from '../commons/CardAlbum.vue';


export default {
  
  name: "AlbumSection",
 

  data() {
        return {
            albums: [],
        };
    },

  components: { 
    CardAlbum 
    },

  // importare api 
  created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
            this.albums = response.data.response
            console.log(this.albums);
        })
        .catch((error) => {
            // handle error
            console.log(error);
        });
    }
}


</script>

<style lang="scss" scoped>
section{
  padding: 100px 0px;
  text-align: center;
  color:white;

  .col__custom{
    width: calc((100% / 5) - 20px);
    margin: 10px;
  }
}
</style>