<template>
  <div id="app">
    <HelloWorld msg="Olá, tudo bem?"/>
    <button @click="toggleMessage">Clique aqui</button>
    <p v-if="showMessage">Aqui vai alguma feature!!!</p>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {
    return {
      showMessage: false
    }
  },
  methods: {
    toggleMessage() {
      this.showMessage = !this.showMessage;
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
  color: #2a7bcc;
  margin-top: 80px;
}
</style>
