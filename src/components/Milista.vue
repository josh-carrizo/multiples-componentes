<template>
<div class="jumbotron">
    <div class="card">
        <h4>{{ titulo }}</h4>
        <ul>
        <li v-for="(enlace, i) in enlaces" :key="i"><a href="enlace.url">{{ enlace.texto }}</a></li>
        </ul>
    </div>
</div>
</template>
<script>

export default{
    name:"MiLista",
    props: {
    titulo: String,
    enlaces: Array
  }
}
</script>
<style scoped>
    .jumbotron{
        background-size: 100% ;
    }

    .titulo{
        font-weight: bold;
        padding: 20px;
        color:white;
        font-size: 4rem;
        text-decoration: underline;
    }

    .titulo_cuadro, .texto_consulta{
        font-weight: bold;
        font-size: 1.5rem;
        text-align: justify;
    }
    .card{
        color:white;
        display: block ;
        background-color: black;
        align-content: justify;
        opacity: .8;;
        width: 25rem;
        border-radius: 20px;
        border: #04B486 5px solid;
        padding: 2rem;
        margin-left: 51rem;
        margin-top: 5rem;;
        transition: transform .5s;
    }
        .card:hover{
        color:black;
        display: block;
        background-color:#04B486 ;
        opacity: .8;;
        width: 25rem;
        border-radius: 20px;
        border: black 5px solid;
        padding: 2rem;
        margin-left: 51rem;
        transform: scale(1.2);
    }

</style>