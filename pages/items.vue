<template>
    <v-flex>
        <Toolbar />
        <ItemsNav />
        <Tabs />
    </v-flex>
</template>

<script>
import Toolbar from "~/components/Toolbar";
import ItemsNav from "~/components/Items/ItemsNav"
import Tabs from "~/components/Items/Tabs"
export default {
    components: {
        Toolbar,
        ItemsNav,
        Tabs
    }
}
</script>

<style>

</style>
