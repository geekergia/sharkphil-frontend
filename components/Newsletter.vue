<template>
  <v-container fluid class="black">
    <v-row>
      <v-col cols="12">
        <v-row align="center" justify="center" class="black">
          <v-flex sm6 md3 style="color: white"><span style="color: orange">Get updated </span> with our latest products & promos</v-flex>
          <v-col cols="12" sm="6" md="3">
            <v-text-field placeholder="your email here" solo v-model="email"></v-text-field>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Newsletter",
  data: () => ({
    email: "",
  })
};
</script>