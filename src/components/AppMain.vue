<script>
import { store } from '../store.js';

export default {
    data() {
        return {
            store
        };
    },
    props: {
        allCards: Array
    }
}
</script>

<template>
    <main class="bg-warning text-dark">
        <div class="container">
            <!--Input-->
            <div class="row pt-3 pb-3">
                <div class="col-2">
                    <div class="form-group">                    
                        <select class="form-control" id="TypeOfCard">
                            <option>Alien</option>
                            <option>Monstre</option>
                            <option>Magic Card</option>
                            <option>Trap Card</option>
                            <option>Dark</option>
                        </select>
                    </div>
                </div>
            </div>     
        </div>
        <!--Card-->
        <div class="container bg-light text-dark">
            <div class="row">
                <div class="col-12 bg-dark text-white pt-3 pb-3">
                    Found 39 cards
                </div>

                <div class="col-12 col-sm-3 text-center"
                v-for="(cards, i) in store.cards"
                :key="i">
                    <div class="single-card">
                        <div>
                            <img :src="cards.image_url" :alt="cards.name">
                        </div>
                        <div>
                            {{cards.name}}
                        </div>
                        <div>
                            {{cards.archetype}}
                        </div>
                        
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
</style>
