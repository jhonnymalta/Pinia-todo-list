<template>
  <div class="task">
    <h3>{{ task.title }}</h3>
    <div class="icons">
      <i class="material-icons" @click="taskStore.delete(task.is)">delete</i>
      <i
        class="material-icons"
        @click="taskStore.toggleFav(task.id)"
        :class="{ active: task.isFav }"
        >favorite</i
      >
    </div>
  </div>
</template>

<script setup>
import { useTaskStore } from "../stores/TaskStore";

const props = defineProps(["task"]);

const taskStore = useTaskStore();
</script>

<style scoped></style>
