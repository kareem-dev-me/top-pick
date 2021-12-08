<template>
  <marquee>
    <v-img
      v-for="(image, index) in images"
      :key="index"
      :src="image"
      height="300"
      width="300"
      class="mx-2 rounded-lg d-inline-block"
      position="top"
      eager
    ></v-img>
  </marquee>
</template>

<script>
export default {
  data() {
    return {
      images: [
        '/logo.png',
        require('~/assets/pexels-monstera-5996954.jpeg'),
        require('~/assets/pexels-anete-lusina-6331144.jpeg'),
        require('~/assets/pexels-cottonbro-6466228.jpeg'),
        require('~/assets/pexels-cottonbro-6466482.jpeg'),
        '/logo.png',
        require('~/assets/pexels-polina-tankilevitch-4440568.jpeg'),
        require('~/assets/pexels-rodnae-productions-5591859.jpeg'),
        require('~/assets/pexels-karolina-grabowska-4239103.jpeg'),
        require('~/assets/pexels-monstera-5331123.jpeg'),
        '/logo.png',
      ],
    }
  },
}
</script>

<style></style>
