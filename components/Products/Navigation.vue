<template>
  <v-layout column ma-1>
    <v-layout ml-6 row fill-height>
      <v-flex class="mr-2" d-flex flex-row-reverse xs1 >
        <v-menu offset-y>
          <template v-slot:activator="{ on }">
            <v-btn text small v-on="on">
              <span class="font-weight-bold">CATEGORIES</span>
              <v-img class="nav-btn ml-2" :src='require("~/assets/icons/products_navigation.png")' max-width="12" max-height="12"/>
            </v-btn>
          </template>
          <v-list>
            <v-list-item
              v-for="(item, index) in items"
              :key="index"
            >
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
      </v-flex>
      <span class="mx-2 grey--text">|</span>
      <v-flex class="ml-2" xs5>
        <v-breadcrumbs class="mt-1" :items="breadcrumb_items" divider=">"></v-breadcrumbs>
      </v-flex>
    </v-layout>
  </v-layout>
</template>


<script>
export default {
  data: () => ({
    breadcrumb_items: [
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
    items: [
        { title: 'Exterior' },
        { title: 'Interior' }
      ],
  }),
}
</script>

<style scoped>

.v-breadcrumbs{
  padding: 0px !important;
}


</style>
