<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Milista titulo="Museos visitados" :enlaces="enlaces__realizado" />
    <Milista titulo="Museos por visitar" :enlaces="enlaces_por_hacer" />
    <br> <br> <br>
  </div>
</template>

<script>
import Milista from './components/Milista.vue'

export default {
  name: 'App',
  components: {
    Milista
  },
  data: () => {
    return {
      // acá están mis datos
      enlaces__realizado: [
        {url: "https://www.paris.es/museo-louvre",texto:"Louvre"},
        {url: "https://www.museumsportal-berlin.de/es/museos/pergamonmuseum/", texto:"Pergamo"},
        {url: "https://www.mim.cl/", texto:"MIM"},
      ],
      enlaces_por_hacer: [
        {url: "https://www.metmuseum.org/", texto: "Metropolitan Museum of Art"},
        {url: "http://www.san-petersburgo.com/hermitage.htm", texto: "Hermitage"},
        {url: "https://www.khm.at/", texto: "Kunsthistorisches"},
        {url: "https://www.egipto.net/museo-egipcio-el-cairo", texto: "Egipcio del Cairo"}
      ],
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>