
<template>
  <h1>{{ title }}</h1>
  <p>welcome..</p>
  <div v-if="showModal">
  <Modal :header="header" :text="text" theme="sale" @close="toggleModal"/>
</div>
  <button @click="toggleModal">open modal</button>
</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: {
    Modal
  },
  data() {
    return {
      title: 'my first vue app 🥳',
      header: 'sign up for the giveaway',
      text: 'grab your swag for half price',
      showModal: false
    }
  },
  methods: {
    handleClick(){
      this.$refs.name.classList.add('active')
      this.$refs.name.focus()
    },
    toggleModal(){
      this.showModal = !this.showModal
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
