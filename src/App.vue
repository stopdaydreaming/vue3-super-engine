<template>
  <h1>{{ title }}</h1>
  <br />
  <input type="text" ref="name">
  <button @click="handleClick">click me!</button>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      title: 'my first vue app :)'
    }
  },
  methods: {
    handleClick(){
      this.$refs.name.classList.add('active')
      this.$refs.name.focus()
    }
  }
}
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
} 
</style>
