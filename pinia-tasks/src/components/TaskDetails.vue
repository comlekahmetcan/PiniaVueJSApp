<script setup>
import { useTaskStore } from "../stores/TaskStore";

const taskStore = useTaskStore();

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
      <span
        class="material-symbols-outlined icon"
        @click="taskStore.deleteTask(task.id)"
      >
        delete
      </span>
      <span
        class="material-symbols-outlined icon"
        @click="taskStore.toogleFav(task.id)"
      >
        favorite
      </span>
    </div>
  </div>
</template>
