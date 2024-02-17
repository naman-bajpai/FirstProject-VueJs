<template>
  <div>
    <h4>
      The current count is {{ count }}; 
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