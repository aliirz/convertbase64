<template>
    <div>
      <p>Text Area</p>
      <p>Result</p>
      <button>Convert</button>
    </div>
  </template>
  
  <script lang="ts">
  import { defineComponent } from 'vue'
  
  export default defineComponent({
    name: 'ConverTo64',
    props: {
      text: {
        type: String,
        required: false
      },
      result: {
        type: String,
        required: false
      }
    }
  })
  </script>