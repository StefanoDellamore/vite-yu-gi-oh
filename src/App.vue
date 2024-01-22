<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import axios from 'axios';

export default {
    data() {
        return {
            baseUrl: 'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0',
            cards: [],
        };
    },
    components: {
        AppHeader,
        AppMain,
        AppFooter
    },  
    methods: {

    },
    
    created() {
        axios
        .get(this.baseUrl)
        .then((response) => {            
            this.cards = response.data.data;
            console.log(this.cards);
        });
    },

}
</script>

<template>

    <AppHeader />

    <AppMain :allCards="cards" />

    <AppFooter />
</template>

<style lang="scss">
@use "assets/scss/main" as *;
@use "assets/scss/partials/reset" as*;
</style>
