<template>
  <v-sheet
    class="mx-auto"
    elevation="8"
  >
    <v-layout row fill-height>
      <v-flex class="title-row">
        <span class="shark-title"> Other Shark Products </span>
        <v-btn text small class="explore-btn" color="orange" to="/" >Explore all →</v-btn>
      </v-flex>
    </v-layout> 
    <v-slide-group
      v-model="model"
      class="pa-4"
      mandatory
      show-arrows
      center-active
    >
      <v-slide-item
        v-for="n in 15"
        :key="n"
        v-slot:default="{ active, toggle }"
      >
        <v-card flat class="mx-auto" max-width="300" style="padding: 20px;" @click="toggle">
          <v-img
            height="300px"
            src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
          >
          </v-img>
          <v-card-text>
            <span class="product-name"> product name here </span>
            <br>
            <span class="price"> price here </span>
          </v-card-text>
        </v-card>
      </v-slide-item>
    </v-slide-group>
  </v-sheet>
</template>

<script>
  export default {
    data: () => ({
      model: null,
    }),
  }
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Exo+2:300,400,400i,500,600,700&display=swap');

* {
  font-family: 'Exo 2', sans-serif;
} 

.title-row{
  margin-left: 30px;
  margin-top: 20px;
}

.explore-btn{
  margin-left: 50px;
}

.shark-title{
  margin-top: 50px;
  font-size: 25px;
}

</style>