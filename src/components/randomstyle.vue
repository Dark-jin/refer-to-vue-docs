<script setup>
import { reactive, ref } from '@vue/reactivity';

const fontSize = ref(30);

const styleObject = reactive({ color: 'blue', fontSize: '20px' });
</script>
<template>
   <div>
      <div :style="{ 'font-size': fontSize + 'px' }">Hello Custom</div>
      <div :style="styleObject">Su</div>
   </div>
</template>
