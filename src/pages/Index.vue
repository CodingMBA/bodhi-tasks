<template>
  <q-page padding>
    <input type="text" v-model="message" @keyup.esc="clearMessage" @keyup.enter="alertMessage" />
    <button @click="clearMessage">Clear</button>
    <h5 class="border-gray" v-show="message.length">{{ message }}</h5>
  </q-page>
</template>

<script>
export default {
  data() {
    return {
      message: 'I love Vue.js!',
    }
  },
  methods: {
    clearMessage() {
      this.message = ''
    },
    alertMessage() {
      alert(this.message)
    },
  },
}
</script>

<style>
.border-gray {
  border: 1px solid gray;
}
</style>
