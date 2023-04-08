<template>
    <div id="main-containers-quizs">
        <div class="main-container-quiz" style="animation: efeito-one 0.5s;">
            <!-- <router-link to="/a"> -->
                <!-- <p></p> -->
                <router-link to="TesteInterligenciaArtificial">Que tipo de Inteligência Artificial você seria no futuro? Descubra agora!</router-link>
                <img src="https://img.quizur.com/f/img6419a59be4b4b1.29687114.jpg?lastEdited=1679402398" alt="">
            <!-- </router-link> -->
        </div>
        <div class="main-container-quiz" style="animation: efeito-one 1s;">
            <router-link to="TesteVicioEmTecnologia">Vício em Tecnologia</router-link>
            <img src="https://img.quizur.com/f/img6362c1ab109915.45105346.jpg?lastEdited=1667416495" alt="">
        </div>
        <div class="main-container-quiz" style="animation: efeito-one 1.5s;">
            <router-link to="TesteQI">Qual seu QI?</router-link>
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQLkvVmlnU2OIcne3FhCS4W7SL_LGn38hPBE5MaWv_0B84EdkdXcnXdVObOflMI9E2Z0bU&usqp=CAU" alt="">
        </div>
        <div class="main-container-quiz" style="animation: efeito-one 2s;">
            <router-link to="TesteViajemParaOFuturo">Descubra o que você faria se pudesse viajar para o futuro!</router-link>
            <img src="https://img.quizur.com/f/img640265ee7648a9.63333071.jpg?lastEdited=1677878775" alt="">
        </div>
    </div>
</template>

<script>
    export default {
        name: 'App'
    }
</script>

<style scoped>
    * {
        margin: 0;
        padding: 0;
    }
    
    #main-containers-quizs {
        display: flex;
        justify-content: space-around;
    }
    .main-container-quiz {
        border: 1px solid white;
        padding: 1px;
        width: 100%;
        height: 200px;
        margin: 1px;
        cursor: pointer;
        display: flex;
        justify-content: center;
        align-items: end;
    }
    .main-container-quiz:hover {
        box-shadow: 13px 13px 5px rgb(7, 7, 130);
        transition-duration: .3s;
    }
    .main-container-quiz a {
        background-color: white;
        padding: 3px;
        color: black;
        position: absolute;
        width: 300px;
        text-align: center;
        margin-bottom: 20px;
        text-decoration: none;
    }

    img {
        width: 100%;
        height: 100%;
    }
</style>