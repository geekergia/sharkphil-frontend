<template>
  <v-layout column ma-2>
    <v-layout row fill-height>
      <v-flex class="mr-2" d-flex flex-row-reverse xs1 >
        <span>Categories</span>
      </v-flex>
      <span class="mx-2">|</span>
      <v-flex class="ml-2" xs5>
        <v-breadcrumbs class="mt-1" :items="items" divider=">"></v-breadcrumbs>
      </v-flex>
    </v-layout>
  </v-layout>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        text: 'Home',
        disabled: false,
        href: '/',
      },
      {
        text: 'Link 1',
        disabled: false,
        href: 'breadcrumbs_link_1',
      },
      {
        text: 'Link 2',
        disabled: true,
        href: 'breadcrumbs_link_2',
      },
    ],
  }),
}
</script>

<style scoped>

.v-breadcrumbs{
  padding: 0px !important;
}
</style>
