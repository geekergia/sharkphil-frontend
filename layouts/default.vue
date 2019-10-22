<template>
  <v-app>
    <v-system-bar color="grey darken-4" dark>
      <span class="white--text">
        <v-icon color="orange darken-2">mdi-phone</v-icon>CALL (02) 372 24 64
      </span>&nbsp;
      <span class="grey--text" style="margin-left: 5px">Mon-Sat 09:00 - 18:00 PHT</span>
      <v-spacer />
      <span class="white--text">
        <v-icon color="orange darken-2">mdi-check-circle</v-icon>Premium Car Accessories Quality Approved By Car Makers And Dealers
      </span>
      <v-spacer />
      <span class="white--text">
        <v-icon color="orange darken-2">mdi-facebook</v-icon>Sharkphil
      </span>
    </v-system-bar>
    <nuxt />
    <v-footer dark>
      <span>&copy; Shark Philippines {{ new Date().getFullYear() }}</span>
      <v-spacer />
      <span class="font-italic title font-weight-bold	">
        <span style="color: #FF921E">/ </span> RULE <span style="color: #FF921E"> THE </span> ROAD
      </span>
      <v-spacer />
      <!-- change to links -->
      <span>About Us | Privacy | Terms of Service</span> 
    </v-footer>
  </v-app>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Exo+2:300,400,400i,500,600,700&display=swap');

* {
  font-family: 'Exo 2', sans-serif;
} 
</style>
</style>

