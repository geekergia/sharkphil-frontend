<template>
  <v-app>
    <v-system-bar color="grey darken-4" dark>
      <span>
        <v-icon color="orange darken-2">mdi-phone</v-icon>CALL (02) 372 24 64
      </span>&nbsp;
      <span class="grey--text">Mon-Sat 9:00 - 10:00 PHT</span>
      <v-spacer />
      <span>
        <v-icon color="orange darken-2">mdi-check-circle</v-icon>Premium Car Accessories Quality Approved By Car Makers And Dealers
      </span>
      <v-spacer />
      <span>
        <v-icon color="orange darken-2">mdi-facebook</v-icon>Sharkphil
      </span>
    </v-system-bar>
    <nuxt />
    <v-footer dark >
      <span>&copy; Shark Philippines {{ new Date().getFullYear() }}</span>
      <v-spacer />
      <span>
        <strong>RULE THE ROAD</strong>
      </span>
      <v-spacer />
      <span>About Us | Privacy | Terms of Service</span>
    </v-footer>
  </v-app>
</template>

