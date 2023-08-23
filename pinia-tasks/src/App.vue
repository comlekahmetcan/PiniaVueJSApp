<template>
  <main>
    <!-- heading -->
    <header>
      <img src="./assets/pinia-logo.svg" alt="pinia logo" />
      <h1>Pinia Tasks</h1>
    </header>

    <!-- task list -->

    <div class="task-list">
      <div v-for="task in taskStore.tasks">
        <p>{{ task.title }}</p>
      </div>
    </div>
  </main>
</template>

<script setup>
import { useTaskStore } from "./stores/TaskStore";
const taskStore = useTaskStore();
</script>
