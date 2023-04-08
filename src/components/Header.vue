<template>
    <div id="menu">
        <ul class="menu-list">
            <li class="menu-list-item"><router-link to="/">Início</router-link></li>
            <li class="menu-list-item"><router-link to="/">Quiz</router-link></li>
            <li class="menu-list-item"><router-link to="/">Sobre mim</router-link></li>
            <li class="menu-list-item"><router-link to="/aa">Contato</router-link></li>
        </ul>
        <!-- <form action="" disabled>
            <fieldset disabled>
                <label for="">Nome</label>
            <input type="text" name="" id="">
            <button>OK</button>
            </fieldset>
        </form> -->
        <!-- PEGUEI ESSE CODE DA PROVA, MAS ACHEI INTERESSSANTE, POR ISSO DEIXEI COMENTADO AQUI. -->
    </div>
</template>


<script>
    export default {
        name: 'Header'
    }
</script>

<style scoped>
    .menu-list {
        list-style: none;
        display: flex;
        justify-content: space-around;
    }

    .menu-list-item a {
        color: white;
        text-decoration: none;
    }
</style>