<template>
  <div class="p-6">
    <h1 class="text-3xl font-bold mb-4 text-white">My Gallery</h1>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4">
      <div v-for="(image, index) in images" :key="index" class="overflow-hidden rounded-xl shadow-md">
        <img :src="image" alt="Gallery image" class="w-full h-64 object-cover transition-transform duration-300 hover:scale-105" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'GalleryView',
  data() {
    return {
      images: [
        '/img/8.jpg',
        '/img/9.jpg',
        '/img/10.jpg',
        '/img/11.jpg',
        '/img/12.jpg',
        '/img/13.jpg',
        '/img/14.jpg',
        '/img/15.jpg',
        '/img/16.jpg',
        '/img/17.jpg',
      ]
    }
  }
}
</script>
