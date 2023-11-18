<script setup>
import { ref } from 'vue';
let id = 0;

const tasks = ref([
    { id: id++, text: "Task 1", isCompleted: false },
    { id: id++, text: "Task 2", isCompleted: false },
    { id: id++, text: "Task 3", isCompleted: false },
    { id: id++, text: "Task 3", isCompleted: false }
]);

</script>

<template>
    <div class="container">
        <ul>
            <li v-for="task in tasks" :key="task.id"><input type="checkbox" /> {{ task.text }}</li>
        </ul>
    </div>
</template>