<template>
    <div class="content float-left w-8/12 align-middle">
        <div class="m-6 flex">
            {{$route.params.id}}
            <p>{{ photo.id }}</p>
            <p>{{ photo.title }}</p>
            <p>{{ photo.url }}</p>
        </div>
    </div>
</template>

<script>
import dataPhotos from '@/dummy/photos'

export default {
  name: 'DetailPhoto',
  data() {
    return {
        photo: []
    }
  },
  created(){
    this.photo = dataPhotos.filter((photo) => photo.id == this.$route.params.id)[0];
    console.log(this.photo)
  }  
}
</script>

<style scoped>

</style>