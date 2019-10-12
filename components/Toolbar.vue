<template>
    <v-app-bar dark  color="black">
        <router-link to="/">
            <v-img :src='require("~/assets/images/topbar_sharklogo.png")' to="/" max-width="200" max-height="200" ></v-img>
        </router-link>
        <v-spacer />
        <v-toolbar-items>
            <div class="bar">
                <input class="search-bar" type="text" name="searchbar" placeholder="Search Items">
                <input class="search-btn" type="image" :src='require("~/assets/icons/search_inactive.png")' width="20px" height="20px" alt="">
            </div>
            <v-btn to="/products" text>Products</v-btn>
            <v-btn text>Customize</v-btn>
            <v-btn color="orange darken-2">
            <v-icon>mdi-car-back</v-icon>
            </v-btn>
        </v-toolbar-items>
    </v-app-bar>
</template>

<script>
export default {
  name: "Toolbar",
  data() {
    return {

    };
  }
};
</script>

<style>
.img-box {
    color: grey;
}

.bar{
    margin-top: 15px;
    margin-right: 350px;
}

.search-bar{
    width: 300px;
    height: 30px;
    background-color: #4D4D4D;
}

.search-btn{
}

#Append{
    height: 10px !important;
    width: 10px !important;
}
</style>


    
