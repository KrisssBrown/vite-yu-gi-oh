<template>
    <header class="container">
        <div class="logo-container">
            <img src="/Yu-Gi-Oh.png" class="logo">
        </div>

        <h1>
            Yu-Gi-Ho
        </h1>
    </header>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
header {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 48px;
    // background-color: rgba($color: #000000, $alpha: 0.3);

    .logo-container{
        height: 100%;
    }

    h1{
        color: white;
        justify-self: center;
    }
}
</style>