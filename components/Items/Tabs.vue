<template>
  <v-card>
    <v-tabs
        v-model="currentItem"
        background-color="transparent"
    >
        <v-tab
        v-for="item in items"
        :key="item"
        :href="'#tab-' + item"
        >
        {{ item }}
        </v-tab>
    </v-tabs>

    <v-tabs-items v-model="currentItem">
      <v-tab-item
        v-for="item in items.concat(more)"
        :key="item"
        :value="'tab-' + item"
      >
        <v-card flat>
          <v-card-text class="font-weight-bold">
            {{ text }}
          </v-card-text>
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </v-card>
</template>

<script>
  export default {
    data: () => ({
      currentItem: 'tab-DESCRIPTION',
      items: [
        'DESCRIPTION', 'SIZE DETAILS', 'DELIVERY INFO', 'PAYMENT OPTIONS',
      ],
      more: [
        'News', 'Maps', 'Books', 'Flights', 'Apps',
      ],
      text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'
    }),
  }
</script>

<style>

</style>
