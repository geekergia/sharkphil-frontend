<template>
  <v-layout column>
    <v-flex>
      <v-app-bar dark  color="black">
        
        <h1>LOGO HERE</h1>

        <v-toolbar-title>Car Accessories</v-toolbar-title>

        <v-spacer />
        <v-toolbar-items>
          <v-btn text>Products</v-btn>
          <v-btn text>Customize</v-btn>
          <v-btn color="orange darken-2">
            <v-icon>mdi-car-back</v-icon>
          </v-btn>
        </v-toolbar-items>
      </v-app-bar>
      <CarCarousel />
      <StartCustomization />
      <OtherSharkProducts />
    </v-flex>
  </v-layout>
</template>

<script>
import CarCarousel from "~/components/CarCarousel";
import StartCustomization from "~/components/StartCustomization";
import OtherSharkProducts from "~/components/OtherSharkProducts";
export default {
  components: {
    CarCarousel,
    StartCustomization,
    OtherSharkProducts
  }
};
</script>
