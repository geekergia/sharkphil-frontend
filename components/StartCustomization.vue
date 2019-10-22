<template>
  <v-layout column ma-3>
    <div id="learnmore">
      <v-layout class="car-layout" row fill-height>
        <v-flex class="car-img" d-flex flex-row-reverse xs5 >
          <v-img :src='require("~/assets/images/home_car_image.png")'
                max-width="450"
                max-height="300"
          ></v-img>
        </v-flex>
        <v-flex class="car-text pa-md-4 mx-lg-auto" xs5>
          <span class="top" style="color: #FF921E">Find Your Setup</span>
          <br /><span class="top grey--text">Show Your Style</span>
          <br />
          <br /><span class="subtitle-1 grey--text" >Customize your style with available Shark Accessories
            <br />Take a look realtime at your set-up as you mix and match
          </span>
        </v-flex>
      </v-layout>
      <v-flex style="border-radius: 2px; border: 1px solid orange">
        <v-card>
          <v-layout align-center justify-space-around row fill-height>
            <v-flex xs2>
              <v-autocomplete label="manufacturer" :items="manufacturers"></v-autocomplete>
            </v-flex>
            <v-flex xs2>
              <v-autocomplete label="model" :items="model"></v-autocomplete>
            </v-flex>
            <v-flex xs2>
              <v-autocomplete label="color" :items="color"></v-autocomplete>
            </v-flex>
          <v-btn dark color="orange darken-2">
              Start Customization
          </v-btn>
          </v-layout>
        </v-card>
      </v-flex>
    </div>
  </v-layout>
</template>

<script>
export default {
  name: "StartCustomization",
  data() {
    return {
      manufacturers: ["Nissan", "Ford", "Nintendo"],
      model: ["Camry", "Starex", "Switch"],
      color: ["Red", "Blue", "Green"]
    };
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Exo+2:300,400,400i,500,600,700&display=swap');

.top{
  font-size: 40px;
  font-style: italic;
}

.car-layout{
  margin-top: 30px;
  margin-bottom: 30px;
}

.car-text{
  margin-left: 0 !important; 
  margin-top: 40px;
  margin-right: 50px;
}

.car-img{
  margin-left: 100px;
}
</style>
