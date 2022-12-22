
<template>
  <h1>{{ title }}</h1>
  <p>welcome..</p>

  <!-- modal #1 -->
  <teleport to=".modals" v-if="showModal">
    <Modal theme="sale" @close="toggleModal">
      <template v-slot:links>
        <a href="#">sign up</a>
        <a href="#">more info</a>
      </template>
      <h1>Super Giveaway</h1>
      <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolorum sunt modi sit nulla id illum placeat quo
        assumenda consequatur nostrum deleniti ab eligendi natus culpa aperiam eum, laboriosam corporis officia!</p>
    </Modal>
  </teleport>

  <!-- modal #2 -->
  <teleport to=".modals" v-if="showModalTwo">
    <Modal @close="toggleModalTwo">
      <template v-slot:links>
        <a href="#">sign up</a>
        <a href="#">more info</a>
      </template>
      <h1>Super Newletter</h1>
      <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolorum sunt modi sit nulla id illum placeat quo
        assumenda consequatur nostrum deleniti ab eligendi natus culpa aperiam eum, laboriosam corporis officia!</p>
    </Modal>
  </teleport>

  <button @click="toggleModal">open modal #1</button><br />
  <button @click="toggleModalTwo">open modal #2</button><br />
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
      showModal: false,
      showModalTwo: false
    }
  },
  methods: {
    handleClick() {
      this.$refs.name.classList.add('active')
      this.$refs.name.focus()
    },
    toggleModal() {
      this.showModal = !this.showModal
    },
    toggleModalTwo() {
      this.showModalTwo = !this.showModalTwo
    }
  }
}
</script>

<style scoped>
#app, #modals {
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
