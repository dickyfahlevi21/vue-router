

<template>
    <div class="content float-left w-8/12 align-middle">
        <div class="m-6 flex">
            <p>{{ post.id }}</p>
            <p>{{ post.title }}</p>
            <p>{{ post.body }}</p>
        </div>
    </div>
    <!-- aku belum buat design detail nya, ku buat dulu ya -->
</template>

<script>
import dataPosts from '@/dummy/posts'

export default {
  name: 'DetailPost',
  data() {
    return {
        post: []
    }
  },
  created(){
    this.post = dataPosts.filter((post) => post.id == this.$route.params.id)[0];
    console.log(this.post)
  }  
}
</script>

<style scoped>

</style>