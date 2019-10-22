<template>
    <v-layout column ma-2>
        <v-layout row fill-height>
            <v-flex mt-4 d-flex flex-row-reverse xs1 >
                <v-btn style="margin-right:32px" depressed text small>
                    <v-img class="nav-btn" :src='require("~/assets/icons/products_navigation_left.png")' max-width="12" max-height="12"/>
                    <span to='/products' class="font-weight-bold">BACK</span>
                </v-btn>
            </v-flex>
            <v-flex >
                <v-breadcrumbs :items="breadcrumb_items" divider="/"></v-breadcrumbs>
            </v-flex>
        </v-layout>

        <v-layout ma-5 row fill-height>
            <v-flex d-flex flex-row-reverse xs7 >
                <v-carousel light hide-delimiters prev-icon="depressed mdi-arrow-left" next-icon="mdi-arrow-right" clear>
                    <v-carousel-item
                    v-for="(item,i) in items"
                    :key="i"
                    :src="item.src"
                    >
                    <div class="img-num font-weight-light">{{ i + 1 }}/4</div>
                    </v-carousel-item>
                </v-carousel>
            </v-flex>
            <v-flex xs3 ml-7 >
                <p class="grey--text font-weight-bold"> [category] </p>
                <p class="font-weight-bold pt-3" style="margin-top: 10px;font-size:36px"> Fortuner Luxury Set </p>
                <p class="orange--text" style="font-size:36px">P 5,800</p>
                <p class="tags pt-5 grey--text"> SELECT COLORS </p>
                <p class="tags pt-5 grey--text"> [OTHER OPTION ex size] </p>
                <v-autocomplete dense label="Other options" :items="otheroptions" style="width:300px"></v-autocomplete>   
                <v-btn to="/cart" block color="#FF921E" dark>ADD TO CART</v-btn>
            </v-flex>
            <v-flex xs1>
                <v-btn icon href="https://www.facebook.com/sharkphil/" target="_blank">
                    <v-icon> mdi-facebook </v-icon>
                </v-btn>
                <v-btn icon href="https://twitter.com/shark_phil" target="_blank">
                    <v-icon> mdi-twitter </v-icon>
                </v-btn>
                <v-btn icon href="/" target="_blank">
                    <v-icon> mdi-google </v-icon>
                </v-btn>
                <p class="tags pt-5 grey--text" style="margin-top: 205px"> Quantity</p>
                <v-autocomplete dense label="Quantity" :items="otheroptions" style="width:200px"></v-autocomplete>
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
        text: 'Products',
        disabled: false,
        href: '/products',
      },
      {
        text: 'Link 2',
        disabled: true,
        href: 'breadcrumbs_link_2',
      },
    ],
    items: [
    {
    src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
    },
    {
    src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
    },
    {
    src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
    },
    {
    src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
    },
    ],
    otheroptions: [
     'Autocompletes', 'Comboboxes', 'Forms', 'Inputs', 'Overflow Buttons', 'Selects', 'Selection Controls', 'Sliders', 'Textareas', 'Text Fields',
    ],
  }),
}
</script>

<style>
.v-application a{
    color: #FF921E;
}

.v-breadcrumbs__item--disabled{
    color: #4D4D4D;
}

.v-window__prev, .v-window__next{
    background: none !important;
}

.v-window__prev{
    margin-top: 200px;
    margin-left: 705px;
}

.v-window__next{
    margin-right: 40px;
    margin-top: 200px;
}

.img-num{
    font-size: 34px;
    margin-left: 756px;
    margin-top: 420px;
}

.v-btn--fab.v-size--default{
    height: 40px !important;
    width: 40px !important;
}

.tags{
    font-size: 14px;
}
.v-application .primary--text{
    color: #FF921E !important;
}

.v-tabs-slider-wrapper{
    height: 0 !important;

}
</style>
