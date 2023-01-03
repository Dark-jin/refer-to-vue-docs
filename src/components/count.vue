<!-- <script setup>
import { nextTick, reactive } from 'vue';

const state = reactive({ count: 0 });

function increment() {
   state.count++;
   nextTick(() => {}); //useEffect()?
}
</script>
<template>
   <button @click="increment">
      {{ state.count }}
   </button>
</template> -->
<script setup>
import { reactive, ref } from 'vue';

const count = ref(0);
const books = reactive([ref('Vue 3 Guide')]);

console.log(books[0].value);

const map = reactive(new Map([['count', ref(0)]]));

console.log(map.get('count').value);

function increment() {
   count.value++;
}
</script>

<template>
   <button @click="increment">
      {{ count }}
   </button>
</template>
