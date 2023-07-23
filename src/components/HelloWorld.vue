<template>
  <div>
    <h1>Text to Base64 Converter and Back</h1>
    <textarea v-model="inputText"></textarea>
    <button @click="convertToBase64">Convert to Base64</button>
    <textarea v-model="outputText"></textarea>
    <button @click="convertToText">Convert to Text</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  data() {
    return {
      inputText: '',
      outputText: ''
    }
  },
  methods: {
    convertToBase64() {
      this.inputText = btoa(this.inputText)
    },
    convertToText() {
      this.outputText = atob(this.outputText)
    }
  }
})
</script>