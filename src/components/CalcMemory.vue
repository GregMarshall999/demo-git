<template>
    <ul>
        <li v-for="m in memory">{{ m }}</li>
    </ul>
</template>

<script setup>

defineProps({
    memory: {
        type: Array
    }
})

</script>