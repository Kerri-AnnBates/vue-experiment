<script setup>

const props = defineProps({
    completedCount: Number
});

</script>
<template>
    <header>
        <input type="text" placeholder="What do you need to do?" /> <button>Add</button>
        <p>Completed tasks: {{ completedCount }}/20</p>
    </header>
</template>