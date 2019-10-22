<template>
    <v-layout column mt-10>
        <Header />
        <v-divider></v-divider>
        <v-layout v-for="j in 5" :key="j" class="justify-center">
            <v-sheet v-for="n in 4" :key="n">
                <v-card flat class="mx-auto" max-width="390" style="padding: 20px;" to="items" >
                    <v-img
                        height="300px"
                        src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
                    >
                    </v-img>
                    <v-card-text>
                        <span class="product-name"> product name here </span>
                        <br>
                        <span class="price"> price here </span>
                    </v-card-text>
                </v-card>
            </v-sheet>
        </v-layout>
    </v-layout>
</template>

<script>
import Header from "~/components/Products/Header";
export default {
    name: "Body",
    components: {
        Header
    },
    data () {
        return{
            sortby: ["Nissan", "Ford", "Nintendo"], 
            pages: [1,2,3,4,5]
        };
    }
};
</script>

<style>

.pages{
    margin-top: 15px;
    margin-left: 20px;
    margin-right: 10px;
}

</style>
