<template>
  <v-layout column ma-3>
    <v-layout row fill-height>
      <v-flex xs5>IMAGE HERE</v-flex>
      <v-flex xs7>
        Find Your Setup
        <br />Show Your Style
        <br />Customize your style with available Shark Accessories
        <br />Take a look realtime at your set-up as you mix and match
      </v-flex>
    </v-layout>
    <v-flex style="border-radius: 2px; border: 1px solid orange">
      <v-card>
        <v-layout align-center justify-space-around row fill-height>
          <v-flex xs2>
            <v-autocomplete label="Manufacturer" :items="manufacturers"></v-autocomplete>
          </v-flex>
          <v-flex xs2>
            <v-autocomplete label="Model" :items="model"></v-autocomplete>
          </v-flex>
          <v-flex xs2>
            <v-autocomplete label="Color" :items="color"></v-autocomplete>
          </v-flex>
        <v-btn dark color="orange darken-2">
            Start Customization
        </v-btn>
        </v-layout>
      </v-card>
    </v-flex>
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
