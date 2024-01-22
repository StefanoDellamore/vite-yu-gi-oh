<script>
export default {
    data() {
        return {

        };
    },
    methods: {

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
                    Fuond 39 cards
                </div>

                <div class="col-12 col-sm-3 text-center" v-for="i in 15" :key="i">
                    carta
                </div>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
</style>
