<script setup lang="ts">
import { ref, onMounted } from 'vue';
import ConvertTo64 from '../components/ConvertTo64.vue';

const jokes = [
  "Why did the Vue instance go to school? To join a new component class!",
  "Why did the Vue developer stay calm? Because he knew how to keep his `state`!",
  "Why did the Vue instance go to school? To join a new component class!",
  "Why did the Vue developer stay calm? Because he knew how to keep his state!",
  "Why was the computer cold? It left its Windows open!",
  "Why was the JavaScript developer sad? Because he didn't Vue the world positively!",
  "How do Vue developers stay fresh? They take v-showers!",
  "Why was the function bad at making friends? It always had strings attached!",
  "How do you comfort a JavaScript bug? You console it!",
  "Why did the developer go broke? Because he used up all his cache!",
  "Why did the Vue component listen to the news? It had a v-bind to current events!",
  "Why was the Vue developer good at fishing? Because of the component hooks!"
  // ... (add more jokes here)
];

const selectedJoke = ref('');
const getRandomJoke = () => {
  const randomIndex = Math.floor(Math.random() * jokes.length);
  selectedJoke.value = jokes[randomIndex];
};

// Call the method when the component is mounted
onMounted(getRandomJoke);
</script>

<template>
  <main class="d-flex flex-column" style="min-height: 100vh;">
    <div class="container flex-grow-1">
      <img alt="ED logo" class="img-fluid mx-auto d-block edlogo" src="../assets/aliirz_Mascot_Generation_for_encodedecode.lol_Name_Byte_the_Bas_f2379a47-5519-4cf8-aadc-31bf80e2d287.png" />
      <h1 class="text-center">EncodeDecode.LOL</h1>
      <p class="text-center">{{ selectedJoke }}</p>
      <ConvertTo64 />
    </div>

    <!-- Sticky Footer -->
    <footer class="bg-light py-3 fixed-bottom">
      <div class="container text-center">
        Made with ❤️ & 🦄 by <a href="https://aliirz.com">aliirz</a>
      </div>
    </footer>
  </main>
</template>
