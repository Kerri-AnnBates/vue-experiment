<script setup>
import { onMounted, ref, watch } from 'vue';
import TaskHeader from './TaskHeader.vue';
import TaskFooter from './TaskFooter.vue';

let id = 0;
let completedCount = ref(0);

const tasks = ref([
    { id: id++, text: "Task 1", isCompleted: false },
    { id: id++, text: "Task 2", isCompleted: false },
    { id: id++, text: "Task 3", isCompleted: false },
    { id: id++, text: "Task 4", isCompleted: false }
]);

// Update completed tasks count.
watch(tasks.value, (completed) => {
    completed = tasks.value.filter(t => t.isCompleted);
    completedCount.value = completed.length
})

// Add task to list
// Clear all tasks
// Clear completed tasks
</script>

<template>
    <div class="container">
        <TaskHeader :completedCount="completedCount" />
        <ul>
            <li v-for="task in tasks" :key="task.id">
                <input type="checkbox" v-model="task.isCompleted" /> {{ task.text }}
            </li>
        </ul>
        <TaskFooter />
    </div>
</template>