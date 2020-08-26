<template>
  <div class="content float-left w-8/12 align-middle">
    <div class="m-6">
      <paginate name="albumPagine" :list="dataAlbum" :per="4" ref="albumPagine" class="grid grid-cols-3">
        <div v-for="(listAlbum, i) in paginated('albumPagine')" :key="i" class="px-3 text-center">
          <img src="../../assets/img/dummy.png" class="w-full">
          <router-link :to="`albums/${listAlbum.id}`" class="text-3xl font-bold">
            <h2 class="p-2">{{ listAlbum.title }}</h2>
          </router-link>
        </div>
      </paginate>
      <paginate-links class="ml-20" for="albumPagine" :limit="4"></paginate-links>  
    </div>
  </div>
</template>

<script>

import dataAlbums from '@/dummy/albums'

export default {
  name: 'Main',
  data() {
    return {
      dataAlbum: dataAlbums
    }
  }
}
</script>