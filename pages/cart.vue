<template>
    <v-flex>
        <Toolbar />
        <CartBanner />
        <CartDetails />
        <Voucher />
    </v-flex>
</template>

<script>
import Toolbar from "~/components/Toolbar";
import CartBanner from "~/components/Cart/CartBanner";
import CartDetails from "~/components/Cart/CartDetails";
import Voucher from "~/components/Cart/Voucher";

export default {
    components: {
        Toolbar,
        CartBanner,
        CartDetails,
        Voucher
    }
}
</script>

<style>

</style>
