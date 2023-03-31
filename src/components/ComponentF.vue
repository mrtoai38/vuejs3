<template>
    <div>
        <h2>F{{ username }}</h2>
    </div>
</template>

<script>
    export default {
        name: 'ComponentF',
        inject: ['username']
    }
</script>

<style scoped>

</style>