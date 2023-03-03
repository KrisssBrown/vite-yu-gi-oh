<template>
    <header class="background">
        <div class="container">
            <div class="logo-container">
                <img :src= "srcLogo"  class="logo">
            </div>
            
            <h1>
                {{ title }}
            </h1>
        </div>
    </header>
</template>

<script>
export default {

    data() {
        return {
            srcLogo: '/Yu-Gi-Oh.png',
            title: 'Yu-Gi-Ho'
        }
    },

}
</script>

<style lang="scss" scoped>

.background{

    background-color: black;
    .container {
        display: flex;
        align-items: center;
        justify-content: center;
        height: 48px;
        gap: 30px;
        // background-color: rgba($color: #000000, $alpha: 0.3);
    
        .logo-container{
            height: 100%;
        }
    
        h1{
            color: white;
            justify-self: center;
        }
    }

}
</style>