<script setup>
import { ref } from 'vue'
const items = ref(['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'])

// TODO: Add Code Here
const add = ref('')
function onDelete(index) {
    return items.value.splice(index,1)
}

function onAdd(item) {
    return items.value.push(item)
}

</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
    <ul>
        <li v-for="(item, index) in items">
            {{ item }}
            <button @click="onDelete(index)" value="index">Delete!</button>
        </li>
    </ul>

    <p><input v-model="add"><button @click="onAdd(add)">Add!</button></p>
   
</template>
