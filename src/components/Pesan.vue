<template>
    <div>
        <p>{{ message }}</p>
        <button @click="changeMessage">Ubah Pesan</button>
    </div>
</template>

<script>
export default {
    name: 'ChangeMessage',
    data() {
        return {
            message: 'Halo, Vue.js'
        }
    },
    methods: {
        changeMessage() {
            this.message = 'Pesan telah diubah!'
        }
    }
}
</script>