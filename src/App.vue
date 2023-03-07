<template>
  <div class="main">
    <div class="main-background">
      <Header/>
    </div>
      <Main/>

  </div>
</template>

<script>
import Main from './components/Main.vue';
import Header from './components/Header.vue';
  export default {
    components:{
      Main,
      Header
    }
    
  }
</script>

<style lang="scss">

@use './style/general.scss' as *;

.main{
  position: relative;
  
  .main-background {
      background-image: url(/CGvgvNH-yugioh-wallpapers-transformed.jpeg);
      background-size: cover;
      background-repeat: no-repeat;    
      height: 100vh;
      width: 100%;
      position: sticky;
      top: 0;
      // bottom: 0;
      z-index: -100;
      // transform: translate(-50%);
      // left: 50%;
      
    }
}


</style>