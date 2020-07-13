<template>
    <div class="jumbotron" id="app">
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
        background: url(https://giffiles.alphacoders.com/208/208893.gif ) no-repeat  center;
        background-size: 100% ;
        height: 45rem;
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
        display: inline-block;
        background-color: black;
        opacity: .8;;
        width: 25rem;
        border-radius: 20px;
        border: white 5px solid;
        padding: 2rem;
        margin: 5rem;
        transition: transform .2s;
    }
        .card:hover{
        color:black;
        display: inline-block;
        background-color: white;
        opacity: .8;;
        width: 25rem;
        border-radius: 20px;
        border: black 5px solid;
        padding: 2rem;
        margin: 5rem;
        transform: scale(1.2);
    }

</style>