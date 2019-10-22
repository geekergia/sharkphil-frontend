<template>
  <v-container class="main-container grey lighten-5">
    <v-row no-gutters>
        <v-col>
          <span class="font-weight-bold" style="font-size: 30px"> Order Details </span>
          <span class="ml-5 font-weight-light" style="font-size: 22px"> 3 ITEMS</span>
          <v-card class="mt-10" outlined flat> 
            <v-container>
              <span class="order-title">WINDSHIELD</span>
              <span class="orange--text font-weight-bold order-title" style="margin-left: 300px">P,1000</span>
              <v-row>
                <v-col class="col-4">
                  <v-img width="150px" height="100px" src="https://cdn.vuetifyjs.com/images/cards/store.jpg"/>
                </v-col>
                <v-col class="col-4">
                  <span class="font-weight-bold" style="font-size: 14px"> Category: </span>
                  <span style="font-size: 14px"> Body Kits</span>
                  <br>
                  <span class="font-weight-bold" style="font-size: 14px"> Quantity: </span>
                  <span style="font-size: 14px"> 1</span> 
                  <br>
                  <span class="font-weight-bold" style="font-size: 14px"> Full Payment: </span>
                  <span style="font-size: 14px"> P1000</span>      
                  <br>
                  <v-btn to="/" text small style="color:#FF921E">Edit</v-btn>
                  <span style="color:#FF921E">|</span>
                  <v-btn to="/" text small style="color:#FF921E">Delete</v-btn>               
                </v-col>
              </v-row>
            </v-container>
          </v-card>
          <br>
          <span class="font-weight-bold"> PARTIAL PAYMENTS? </span>
          <p class="grey--text" style="font-size:12px">
            <br>
            We want to decrease the risk on your part here so we broke big value items into partial payments.
            Complete the balance only after we successfully delivered and/or installed your ordered items. Of course, 
            there's no one stopping you from paying completely upfront.
            <br>
            <br>
            OTHER NOTES
            <br>
            <br>
            Balance are to be paid upon delivery or installation of the items.
          </p>
        </v-col>

        <v-col style="margin-left: 120px">
          <span class="font-weight-bold" style="font-size: 30px"> Delivery Details </span>
          <v-form class="mt-5">
            <v-row>
              <v-col cols="6" sm="6">
                <p class="form-title"> First Name * </p>
                <v-text-field class="delivery-form" v-model="firstname" required :rules="nameRules" single-line outlined />
              </v-col>
              <v-col cols="6" sm="6">
                <p class="form-title"> Last Name * </p>
                <v-text-field class="delivery-form" v-model="lastname" required :rules="nameRules" single-line outlined />
              </v-col>
            </v-row>
            <p class="form-title"> Street Address *</p>
            <v-text-field class="delivery-form" v-model="address" required :rules="addressRules" single-line outlined />
            <p class="form-title"> Appartment, Suite, Unit, Building, Floor (Optional) </p>
            <v-text-field class="delivery-form" v-model="appartment" single-line outlined />
            <v-row>
              <v-col cols="6" sm="6">
                <p class="form-title"> City/Town *</p>
                <v-select class="delivery-form" :items="city_items" :rules="cityRules" flat outlined solo></v-select>
              </v-col>
              <v-col cols="6" sm="6">
                <p class="form-title"> Province * </p>
                <v-select class="delivery-form" :items="province_items" :rules="provinceRules" flat outlined solo></v-select>
              </v-col>
            </v-row>
            <p class="form-title"> Email * </p>
            <v-text-field class="delivery-form" v-model="email" :rules="emailRules" solo flat outlined required></v-text-field>
            <p class="form-title"> Phone Number * </p>
            <v-text-field class="delivery-form" v-model="phonenum" :rules="numberRules" solo flat outlined required></v-text-field>
          </v-form>
          <v-btn class="mt-10" block color="orange" dark>Continue Payment</v-btn>

          <div class="text-left" style="margin-top: 100px;margin-bottom: 30px">
            <v-sheet color="black pa-10" style="color:white">
              <p class="font-weight-bold">/ Do you have a promo code or gift card?</p>
              <v-row>
                <v-text-field label="Enter code here" v-model="promocode" solo flat></v-text-field>
                <v-btn large dark color="grey darken-2">APPLY CODE</v-btn>
              </v-row>
            </v-sheet>
          </div>
        </v-col>
    </v-row>
  </v-container>
</template>
    
<script>
export default {
  data: () => ({
    valid: false,
    firstname: '',
    lastname: '',
    nameRules: [
      v => !!v || 'Name is required',
      v => v.length <= 10 || 'Name must be less than 10 characters',
    ],
    email: '',
    emailRules: [
      v => !!v || 'E-mail is required',
      v => /.+@.+/.test(v) || 'E-mail must be valid',
    ],
    address:'',
    addressRules: [
      v => !!v || 'Address is required',
    ],
    appartment:'',
    city_items: [
      'Item 1',
      'Item 2',
      'Item 3',
      'Item 4',
    ],
    cityRules: [
      v => !!v || 'City/Town is required',
    ],
    province_items: [
      'Item 1',
      'Item 2',
      'Item 3',
      'Item 4',
    ],
    provinceRules: [
      v => !!v || 'Province is required',
    ],
    phonenum: '',
    numberRules: [
      v => !!v || 'Phone number is required',
    ],
    promocode: ''
  }),
}

</script>

<style>
.order-title{
  font-size: 24px;
}

.main-container{
  margin-right: 200px !important;
  margin-top: 50px;
}

.form-title{
  font-size: 14px;
  color: grey;
}
.delivery-form--outlined fieldset{
  border-color: orange;
}
</style>
