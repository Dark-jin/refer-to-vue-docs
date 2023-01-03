<script setup>
import { ref } from 'vue';

const awesome = ref(true);
</script>
<template>
   <div>
      <button @click="awesome = !awesome">changebutton</button>
      <h1 v-if="awesome">Yes Change!</h1>
      <h1 v-else>ReChange!</h1>
   </div>
</template>
