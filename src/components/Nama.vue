<template>
    <div class="Nama">
        <input type="text" v-model="name">
        <h4>Name: {{ name }}</h4>
    </div>
  </template>
  
  <script>
  export default {
    name: 'NamaSaya',
    data() {
        return {
            name: ""
        }
    }
  }
  </script>
  