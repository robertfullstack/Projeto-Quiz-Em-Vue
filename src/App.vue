<template>
  <body>

    <HeaderVue />
    <router-view/>

    <!-- footer -->
  </body>


</template>


<script>
import HeaderVue from './components/Header.vue';
  export default {
    name: 'App',
    components: {
      HeaderVue
    }
  }
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

body {
    font-family: 'Poppins', sans-serif; 
    background: url("../public/images/background-image-01.jpg") no-repeat center;
    background-size: cover;
    height: 100vh;
    color: white;
  } 

  @keyframes efeito-one {
    0% {
      transform: translateX(-1000px);
    }
  }

</style>