<template>
    <div class="card">
        <div class="card-image">
            <img :src="cardImage" alt="">
        </div>
        <div class="card-name">
            {{ cardName }}
        </div>
        <div class="card-archetype">
            {{ cardArchetype }}
        </div>

    </div>
</template>

<script>


export default {
    props: {
        cardImage: {
            type: String,
            required: true
        },

        cardName: {
            type: String,
            required: true
        },

        cardArchetype: {
            type: String,
            required: true
        }
    }
}
</script>

<style lang="scss" scoped>

img{
    max-width: 100%;
}

</style>