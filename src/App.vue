<script setup>
import TaskContainer from './components/TaskContainer.vue'
</script>

<template>
  <div class="wrapper">
    <header>
      <h1>Todo App</h1>
    </header>

    <main>
      <TaskContainer />
    </main>
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
</style>
