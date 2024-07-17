<template>
    <h2>
        First Page Component
    </h2>
    <button @click="addFn('hai')">Add</button>
    <button @click="updateFn(10)">Update</button>
</template>

<script setup lang="ts">
    const emits = defineEmits<{
        (e: 'add', value: string): void
        (e: 'update', id: number): void
    }>()

    function addFn(currentValue: string){
        emits('add', currentValue)
    }

    function updateFn(id: number){
        emits('update', id)
    }
</script>