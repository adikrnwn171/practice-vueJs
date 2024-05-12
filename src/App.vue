<template>
  <div class="image">
    <img alt="Vue logo" src="./assets/logo.png">
  </div>
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <Nama/>
  <Counter/>
  <Pesan/>
  <List/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Nama from './components/Nama.vue'
import Counter from './components/Counter.vue'
import Pesan from './components/Pesan.vue'
import List from './components/List.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Nama,
    Counter,
    Pesan,
    List
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
.hello {
  text-align: center;
}
.image {
  text-align: center;
}
</style>
