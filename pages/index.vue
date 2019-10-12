<template>
  <v-layout column>
    <v-flex>
      <Toolbar />
      <CarCarousel />
      <StartCustomization />
      <OtherSharkProducts />
      <Newsletter />
      <Footer />
    </v-flex>
  </v-layout>
</template>

<script>
import Toolbar from "~/components/Toolbar";
import CarCarousel from "~/components/CarCarousel";
import StartCustomization from "~/components/StartCustomization";
import OtherSharkProducts from "~/components/OtherSharkProducts";
import Newsletter from "~/components/Newsletter";
import Footer from "~/components/Footer";
export default {
  components: {
    Toolbar,
    CarCarousel,
    StartCustomization,
    OtherSharkProducts,
    Newsletter,
    Footer
  }
};
</script>
