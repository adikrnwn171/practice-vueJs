<template>
    <div class="Button-counter">
        <button @click="count++">
            Klik saya {{ count }} kali
        </button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ButtonCounter',
    data() {
        return {
            count: 0
        }
    }
  }
  </script>
  