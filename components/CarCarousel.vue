<template>
  <v-carousel hide-delimiter-background>
    <v-carousel-item v-for="(item,i) in items" :key="i" :src="item.src" continuous>
          <div class="carousel-title text-center font-italic font-weight-bold">BUY ONE TAKE ONE</div>
          <div class="carousel-text text-center pt-5">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean eu porttitor nulla. 
            Vestibulum vel justo at tellus iaculis ultrices et nec ex. Aenean id efficitur lacus. </div>
          <v-hover v-slot:default="{ hover }">
            <div class="learn-more-container pt-5">
              <v-img :src='require("~/assets/images/learn-more-active.png")' to="/" max-width="200" max-height="200" >
                <div class="learn-more text-center font-italic font-weight-bold">Learn more</div>
              </v-img>
              <div v-if="hover" class="hover-reveal">
                <v-img :src='require("~/assets/images/learn-more-hover.png")' to="/" max-width="200" max-height="200" />
              </div>
            </div>
          </v-hover>
  
    </v-carousel-item>
  </v-carousel>
</template>

<script>
import axios from 'axios';

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

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Exo+2:300,400,400i,500,600,700&display=swap');

* {
  font-family: 'Exo 2', sans-serif;
} 

.carousel-title{
  font-size: 72px;
  color: white;
  margin-top: 150px;
}

.carousel-text{
  font-size: 16px;
  color: white;
}

.learn-more-container{
  margin-left: 710px;
}

.learn-more{
  font-size: 16px;
  color: gold;
}

.hover-reveal{
  position: absolute;
}

</style>