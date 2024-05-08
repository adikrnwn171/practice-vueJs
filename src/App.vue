<template>
  <div class="image">
    <img alt="Vue logo" src="./assets/logo.png">
  </div>
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <input type="text" v-model="name">
  <h4>Name: {{ name }}</h4>
  <div>
    <p>{{ message }}</p>
    <button @click="changeMessage">Ubah Pesan</button>
  </div>
  <div>
    <ul>
      <li v-for="item in items" :key="item.id">{{ item.name }}</li>
    </ul>
    <button @click="addItem">Tambah Item</button>
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
      name: "",
      message: 'Halo, Vue.js!!!',
      items: [
        {id: 1, name: 'Buku'},
        {id:2, name: 'Pensil'},
        {id:3, name: 'Penghapus'}
      ]
    }
  },
  methods: {
    changeMessage() {
      this.message = 'Pesan telah diubah!'
    },
    addItem() {
      const newItem = {id: this.items.length+1, name:'Barang Baru'};
      this.items.push(newItem);
    }
  },
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
