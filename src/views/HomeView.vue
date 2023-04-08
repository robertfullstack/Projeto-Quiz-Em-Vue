<template>
  <div id="main-content">
    <div class="main-content" id="block">
      <h1>Desde Suas Inteligências!</h1>
      <button class="main-button-containers" @click="removeBlock">DESBLOQUEAR QUIZS</button>
    </div>
    <div id="main-content-show">
        <figure>
            <router-link to="/Bloqueado" id="block-content"> 
              <img src="../../public/images/cadeado-background-image.png" alt="">
            </router-link>  
        </figure>
      <div id="main-opacity">
        <ContainersQuizsVue />
      </div>
    </div>
  </div>

</template>

<script>
import ContainersQuizsVue from '@/components/ContainersQuizs.vue';
  export default {
    name: 'HomeView',
    components: {
      ContainersQuizsVue
    },
    data() {
      return {
        showQuisz: false
      }
    },
    methods: {
      removeBlock() {
        document.getElementById("block").style.display = "none"
        document.getElementById("block-content").style.display = "none"
        // document.getElementById("main-content-show").style.opacity = "10"
        document.getElementById("main-opacity").style.opacity = "10"

        document.getElementsByTagName("img")[0].style.display = "none"
      }
    }
  }
</script>

<style scoped>
  /* #main-content-show a {
    width: 1000px;
    color: white;
    background: red;
    cursor: none;
  } */

  #main-content {
    margin-top: 70px;
  }

  .main-content {
    display: flex; 
    flex-direction: column;
    text-align: center;
  }

  .main-button-containers {
    width: 50%;
    height: 60px;
    font-size: 24px;
    cursor: pointer;
    margin: 20px auto;
    background: black;
    color: white;
    border: none;
    box-shadow: 3px 3px 5px rgba(0, 0, 255, 0.404);
  }

  #main-opacity {
    opacity: 0.7;
  }
  
  figure {
    margin: 0;
    padding: 0;
  }

  figure a { 
    display: flex;
    justify-content: center;
    width: 97%;
    /* background-color: white; */
    height: 300px;
    position: absolute;
    z-index: 2;
  }
  
  img {
    width: 230px;
    position: absolute;
    z-index: 1;
  }
</style>