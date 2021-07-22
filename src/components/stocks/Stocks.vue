<template>
    <v-layout row wrap>
        <Stock v-for="stock in stocks" :key="stock.name" :stock="stock" />
    </v-layout>
</template>

<script>
import Stock from './Stock.vue'

export default {
    name: 'stocks',
    components: {Stock},
    computed: {
        stocks() {
            return this.$store.getters.stocks
        }
    }
};
</script>

<style>
</style>