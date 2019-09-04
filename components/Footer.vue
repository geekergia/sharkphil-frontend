<template>
  <v-footer padless class="white">
    <v-col cols="12">
      <v-row align="top" justify="space-between" class="black--text">
        <v-card class="ma-3 pa-6" flat>Logo Here</v-card>
        <v-card class="ma-3 pa-6" flat>
          <v-card-title>Products</v-card-title>
          <v-card-text>
            Exterior
            <br />Interior
            <br />Car Care
            <br />Electronics
          </v-card-text>
        </v-card>
        <v-card class="ma-3 pa-6" flat>
          <v-card-title>Service</v-card-title>
          <v-card-text>
            Order Status
            <br />Warranty Policy
            <br />Shipping
            <br />Replacements
            <br />Payment Options
            <br />
          </v-card-text>
        </v-card>
        <v-card class="ma-3 pa-6" flat>
          <v-card-title>Social</v-card-title>
          <v-card-text>
            <v-btn icon outlined color="orange">
              <v-icon color="orange">mdi-facebook-box</v-icon>
            </v-btn>
            <v-btn icon outlined color="orange">
              <v-icon color="orange">mdi-instagram</v-icon>
            </v-btn>
          </v-card-text>
        </v-card>
        <v-card class="ma-3 pa-6" flat>
          <v-card-title>Contact Us</v-card-title>
          <v-card-text>
            shark@email.com
            <br />
            <strong>(02) 372 24 64 (02) 374 36 36</strong>
            <br />Mon-Sat 09:00-18:00 (except holidays)
            <br />1013A EDSA, Project 7, Quezon City
          </v-card-text>
        </v-card>
      </v-row>
    </v-col>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    icons: [
      "fab fa-facebook",
      "fab fa-twitter",
      "fab fa-google-plus",
      "fab fa-linkedin",
      "fab fa-instagram"
    ]
  })
};
</script>