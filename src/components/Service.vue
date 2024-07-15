<template>
    <div>
        <p> {{ service.name }}</p>
    </div>
</template>

<script setup>
    const service = defineProps({
        service:Object
    })
</script>

<style scoped>

</style>