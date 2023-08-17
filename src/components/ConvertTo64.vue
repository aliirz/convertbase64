<template>
  <div>
    <div class="form-group">
        <textarea class="form-control" v-model="inputText" placeholder="Ready for some Base64 sorcery? Input your text!" id="floatingTextarea"></textarea>
        <br />
        <div class="d-flex justify-content-end">
          <button type="button" @click="convertTo64" class="btn btn-primary mr-5">Encode</button>
          <button type="button" @click="convertFrom64" class="btn btn-secondary">Decode</button>
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
      },
      convertFrom64() {
        this.inputText = atob(this.inputText)
      }
    },
    data() {
      return {
        inputText: ''
      }
    }
  })
  </script>