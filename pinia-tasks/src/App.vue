<template>
  <main>
    <!-- heading -->
    <header>
      <img src="./assets/pinia-logo.svg" alt="pinia logo" />
      <h1>{{ taskStore.name }}</h1>
    </header>
  </main>
</template>

<script setup>
import { useTaskStore } from "./stores/TaskStore";
const taskStore = useTaskStore();
</script>
