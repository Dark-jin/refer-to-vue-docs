<script setup>
import TodoItem from './components/todo.vue';
import Counter from './components/count.vue';
import computer from './components/computer.vue';
import Rstyle from './components/randomstyle.vue';
import Conditional from './components/Conditional.vue';
import formoon from './components/formoon.vue';
</script>

<template>
   <div>
      <div id="app">
         <h1>To-Do-List</h1>
         <TodoItem />
      </div>
      <div>
         <Counter />
      </div>
      <computer />
      <Rstyle />
      <Conditional />
      <div>
         <formoon />
      </div>
   </div>
</template>
