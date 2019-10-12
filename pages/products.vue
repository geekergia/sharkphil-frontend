<template>
    <v-layout column>
        <v-flex>
            <Toolbar />
            <TopBanner />
            <Navigation />
            <Body />
        </v-flex>
    </v-layout>
</template>

<script>
import Toolbar from "~/components/Toolbar";
import TopBanner from "~/components/Products/TopBanner";
import Navigation from "~/components/Products/Navigation";
import Body from "~/components/Products/Body";
export default {
  components: {
    Toolbar,
    TopBanner, 
    Navigation,
    Body
  }
};
</script>

<style>

</style>
