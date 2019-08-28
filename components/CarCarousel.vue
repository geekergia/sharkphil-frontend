<template>
  <v-carousel hide-delimiter-background>
    <v-carousel-item v-for="(item,i) in items" :key="i" :src="item.src" continuous/>
  </v-carousel>
</template>

<script>
export default {
  name: "CarCarousel",
  data() {
    return {
      items: [
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg"
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/sky.jpg"
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/bird.jpg"
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/planet.jpg"
        }
      ]
    };
  }
};
</script>
