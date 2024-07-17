<template>
    <h1>Home Component</h1>
    <FirstPage @add="parentAddFn" @update="parentUpdateFn"></FirstPage>
</template>

<script setup lang="ts">
    import FirstPage from "./FirstPageComponent.vue"

    function parentAddFn(value: string){
        alert(value)
    }

    function parentUpdateFn(id: number){
        alert(id)
    }
</script>