<template>
    <div class="content float-left w-8/12 align-middle">
        <div class="m-6 flex">
            {{$route.params.id}}
            <p>{{ album.id }}</p>
            <p>{{ album.title }}</p>
        </div>
    </div>
</template>

<script>
import dataAlbums from '@/dummy/albums'

export default {
  name: 'DetailAlbum',
  data() {
    return {
        album: []
    }
  },
  created(){
    this.album = dataAlbums.filter((album) => album.id == this.$route.params.id)[0];
    console.log(this.album)
  }  
}
</script>

<style scoped>

</style>