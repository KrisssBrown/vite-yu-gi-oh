<!-- v-for="(card, i) in cards" :key="i" -->

<template>
    <main class="background">
        <div class="cards-container">
            <div class="container">
                <div class="grid">
                    <Card v-for="(card, i) in cards" :key="i" :cardImage="card.card_images[0].image_url" :cardName="card.name" :cardArchetype="card.type" class="cards"/>
                </div>
            </div>
        </div>
    </main>
</template>

<script>
import axios from 'axios'
import Filter from './Filter.vue'
import Card from './Card.vue'

export default {
    components: {
        Card,
        Filter
    },

    data() {
        return {
            cards: [],
            // index: 1
        }
    },

    methods: {
        fetchCard() {
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php',{
                params:{
                    num: 20,
                    offset:3500
                }
            }).then((res) => {
                this.cards = res.data.data
                console.log(this.cards)
            })
        }
    },

    // computed: {
    //     cardImage() {
    //         return this.cards.data[0].card_images[0].image_url
    //     },

    //     name() {
    //         return this.cards.data.name
    //     },

    //     archetype() {
    //         return this.cards.data[0].archetype
    //     }
    // },

    created() {
        this.fetchCard()

    },

}
</script>

<style lang="scss" scoped>
.background {
    position: sticky;
        top: 0;

    // .cards-container{
    //     position: sticky;
    //     top: 0;
    // }
}

.container {
    background-color: rgba($color: #000000, $alpha: 0.5);
    padding: 40px;
    height: 100%;

    .grid{
        display: grid;
        grid-template-columns: repeat(5,1fr);
        gap: 20px;
    }
}
</style>