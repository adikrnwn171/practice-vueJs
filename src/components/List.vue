<template>
    <div>
        <tr v-for="item in items" :key="item.id">{{ item.name }} 
            <td><button @click="deleteItem(item.id-1)">Delete</button></td>
        </tr>
        <input type="text" v-model="barang"><br>
        <button @click="addItem">Tambah Item</button>
    </div>
</template>

<script>
export default {
    name: 'RenderingList',
    data() {
        return {
            barang: "",
            items: [
                {id: 1, name: 'Buku'},
                {id: 2, name: 'Pensil'},
                {id: 3, name: 'Penghapus'}
            ]
        }
    },
    methods: {
        addItem() {
            const newItem = {id: this.items.length+1, name: this.barang}
            this.items.push(newItem)
            this.barang = null
        },
        deleteItem(id) {
            this.items.splice(id, 1)
        }
    }
}
</script>