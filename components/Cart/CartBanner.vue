<template>
  <v-card
    flat
    max-width="50000"
    max-height="50000"
    style="background-color: black">
    <v-container class="cart-container">
      <v-row>
        <v-col class="cart-title col-3">
          <span class="your-cart display-2 font-italic font-weight-light" style="color: #FF921E">your cart</span>
        </v-col>
        <v-col class="col-2">
          <v-img :src='require("~/assets/images/checkout_bigslash.png")' to="/" max-width="50" max-height="500" />
        </v-col>    
        <v-col style="margin-top: 20px">
          <span class="cart-text">Sub Total</span>
          <v-btn text small style="color: #FF921E">SEE DETAILS</v-btn>
          <span class="cart-text ml-10">P 31,000</span>
          <!-- <span class="grey--text" style="font-size: 14px; margin-left:400px">TOTAL</span> -->
          <br>
          <span class="balance-text grey--text" >P 40,000 BALANCE</span>
          <br>
          <span class="cart-text">Delivery Fee</span>
          <v-btn icon>
              <v-img :src='require("~/assets/icons/info_overdark.png")' to="/" max-width="20" max-height="20" />
          </v-btn>
          <span class="cart-text" style="margin-left: 75px">P 0</span>
          <br>
          <span class="balance-text grey--text" >( Freighter not included )</span>
        </v-col>   
        <v-col class="col-2"> 
          <p class="grey--text">TOTAL</p>
          <p class="white--text">P 31,000 </p>
        </v-col>
      </v-row>  
    </v-container>
  </v-card>
</template>

<script>
export default {

}
</script>

<style scoped>
.cart-title{
    margin-left: 150px;
    margin-top: 35px;

}
.cart-text{
    color: white;
    font-size: 20px;
}
.cart-container{
    margin-left:0 !important;
    padding: 0 !important;
}

.balance-text{
  margin-left: 250px;
  font-size: 14px;
}

.col-3{
  max-width: 20% !important;
}

</style>
