<script setup>
const props = defineProps({
  task: {
    type: Array,
    required: true,
    default: () => [],
  },
});
</script>

<template>
    
  <div class="task">
    <h3>{{ task.title }}</h3>
    <div class="icons">
      <span class="material-symbols-outlined icon"> delete </span>
      <span class="material-symbols-outlined icon"> favorite </span>
    </div>
  </div>
</template>
