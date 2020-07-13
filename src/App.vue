<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <ExtraInfo titulo="Installed CLI Plugins" v-bind:enlaces="enlaces_cli_plugins" />
    <ExtraInfo titulo="Essential Links" v-bind:enlaces="enlaces_essential_links" />
    <ExtraInfo titulo="Ecosystem" v-bind:enlaces="enlaces_ecosystem" />
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
        {texto: 'babel', url: 'https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel'},
        {texto: 'eslint', url: 'https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint'}
      ],
      enlaces_por_hacer: [
        {url: "https://vuejs.org", texto: 'Core Docs'},
        {url: "https://forum.vuejs.org", texto: 'Forum'},
        {url: "https://chat.vuejs.org", texto: 'Community Chat'},
        {url: "https://twitter.com/vuejs", texto: 'Twitter'},
        {url: "https://news.vuejs.org", texto: 'News'}
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