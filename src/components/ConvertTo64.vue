<template>
  <div>
    <div class="form-group">
        <textarea class="form-control" v-model="inputText" placeholder="Ready for some Base64 sorcery? Input your text!" id="floatingTextarea"></textarea>
        <br />
        <div class="d-flex justify-content-end">
          <button type="button" @click="convertTo64" :disabled="isEncoded" class="btn btn-primary" :style="{ 'marginRight': '10px' }">Encode</button>
          <button type="button" @click="convertFrom64" :disabled="!isEncoded" class="btn btn-secondary">Decode</button>
        </div>
    </div>
  </div>
</template>



  
  <script lang="ts">
  import { defineComponent } from 'vue'
  
  export default defineComponent({
    name: 'ConvertTo64',
    methods: {
      convertTo64() {
       this.inputText = btoa(this.inputText)
       this.isEncoded = true
      },
      convertFrom64() {
        this.inputText = atob(this.inputText)
        this.isEncoded = false
      }
    },
    data() {
      return {
        inputText: '',
        isEncoded: false
      }
    }
  })
  </script>