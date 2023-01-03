<script setup>
import { ref, reactive, computed } from 'vue';

const author = reactive({
   name: 'John Doe',
   books: ['Vue 2 - Advanced Guide', 'Vue 3 - Basic Guide', 'Vue 4 - The Mystery'],
});

// const publishbookmessage = computed(() => {
//    return author.books.length > 0 ? 'Yes' : 'No';
// });
function publish() {
   return author.books.length > 0 ? 'Yes' : 'No';
}
const firstname = ref('Jack');
const lastname = ref('Don');

const fullName = computed({
   //getter
   get() {
      return firstname.value + ' ' + lastname.value;
   },
   //setter
   set(newValue) {
      [firstname.value, lastname.value] = newValue.split(' ');
   },
});
</script>

<template>
   <div>
      <p>Has published books :</p>
      <span>{{ publishbookmessage }}</span>
      <p>{{ publish() }}</p>
      <p>{{ fullName }}</p>
   </div>
</template>
