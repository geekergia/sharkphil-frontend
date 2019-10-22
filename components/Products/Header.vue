<template>
    <v-layout ml-9 row fill-height>
        <v-flex d-flex xs8>
            <div> 
                <span class="font-weight-bold" style="font-size: 28px"> Main Categories </span>
                <br>
                <span class="grey--text" subtitle> 2 items under [category] </span>
            </div>
        </v-flex>
        <v-flex d-flex>
            <v-autocomplete class="sort-btn" ml-10 style="width: 100px" solo flat outlined label="sort by" :items="sortby"></v-autocomplete>
        </v-flex>
        <span class="pages"> Page </span>
        <v-flex xs1>
            <v-combobox outlined solo flat :items="pages" style="width:80px" ></v-combobox>
        </v-flex>
        <span style="margin-top: 15px;"> of 5 </span>
        <v-flex ml-5>
            <v-btn text icon>
                <v-img :src='require("~/assets/icons/products_pagination_left_active.png")'
                    max-width="30"
                    max-height="40"
                ></v-img>          
            </v-btn>
            <v-btn text icon>
                <v-img :src='require("~/assets/icons/products_pagination_right_active.png")'
                    max-width="30"
                    max-height="40"
                ></v-img>  
            </v-btn>
        </v-flex>
    </v-layout>    
</template>

<script>
export default {
    name: "Body",
    data () {
        return{
            sortby: ["Nissan", "Ford", "Nintendo"], 
            pages: [1,2,3,4,5]
        };
    }
}
</script>

<style>
.pages{
    margin-top: 15px;
    margin-left: 20px;
    margin-right: 10px;
}
</style>
