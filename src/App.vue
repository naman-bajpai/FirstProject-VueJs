<template>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Kode+Mono:wght@400..700&display=swap" rel="stylesheet">
  <div>
    <h4>
      The current count is
    </h4>
    <h1 id="count">0</h1>
    <button id="add">+</button>
    <button id="subtract">-</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0
    }
  },
  mounted() {
    document.getElementById('add').addEventListener('click', () => {
      this.count++
      document.getElementById('count').innerText = this.count
    })
    document.getElementById('subtract').addEventListener('click', () => {
      this.count--
      document.getElementById('count').innerText = this.count
    })
  }
}
</script>
<!-- 
<script setup>
import { ref } from 'vue'

const open = ref(false)
</script>

<template>
  <button @click="open = true">Open Modal</button>

  <div v-if="open" class="modal">
    <p>Hello from the modal!</p>
    <button @click="open = false">Close</button>
  </div>
</template>

<style scoped>
.modal {
  position: fixed;
  z-index: 999;
  top: 20%;
  left: 50%;
  width: 300px;
  margin-left: -150px;
}
</style> -->