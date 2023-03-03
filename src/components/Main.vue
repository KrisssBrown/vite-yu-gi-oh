<template>
    <main class="background">
        <div class="container">
            <div class="cards">
                
            </div>
        </div>
    </main>
</template>

<script>
import axios from 'axios'

import Card from './Card.vue'

export default {
    components: {
        Card
    },

    data() {
        return {
            cards: []
        }
    },

    methods: {
        fetchCard() {
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php').then((res) => {
                console.log(res)
            })
        }
    },

    mounted() {

    },

}
</script>

<style lang="scss" scoped>

.background{
    background-image: url(/CGvgvNH-yugioh-wallpapers-transformed.jpeg);
    background-size: cover;
    background-repeat: no-repeat;
    height: calc(100vh - 48px);
    width: 100%;
    .container {
        background-color: rgba($color: #000000, $alpha: 0.5);
        padding: 40px;
        height: 100%;
    }

}
</style>