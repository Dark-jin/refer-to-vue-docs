<script setup>
import { ref } from 'vue';

const parentm = ref('parent');
const items = ref([{ message: 'Foo' }, { message: 'Bar' }, { message: 'Too' }]);

// new Vue({
//    el: '#listit',
//    data: {
//       list: ['mine', 'it', 'record'],
//    },
// });
</script>

<template>
   <div id="test">
      <li v-for="(item, index) in items" v-bind:key="item.id">{{ parentm }} - {{ index }} - {{ item.message }}</li>
   </div>
   <!-- <div id="listit">
      <ui>
         <li v-for="item in items" v-bind:key="item">
            {{ item }}
         </li>
      </ui>
   </div> -->
</template>
