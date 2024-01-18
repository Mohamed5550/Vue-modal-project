<template>
  <h1>{{ title }}</h1>
  <div v-if="showModal">
    <Modal header="This is a test header text" @close="toggleModal">
      <h1>Modal title</h1>
      <p>Modal content</p>
    </Modal>
  </div>

  <button @click="toggleModal">Show modal</button>
</template>

<script>

import Modal from './components/Modal.vue';
import './assets/global.css';

export default {
  name: 'App',
  components: {Modal},
  data() {
    return {
      title: "My first vue app",
      showModal: false
    }
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
