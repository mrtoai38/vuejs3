<template>
    <div>
        <h2>Article components</h2>
        <h2>{{ title }}</h2>
        <h2 v-bind="$attrs">Like: {{ likes }}</h2>
        <h2>Published: {{ isPublished ? 'Yes' : 'No' }}</h2>
    </div>
</template>

<script>
    export default {
        name: 'Article',
        props: {
            title: {
                type: String,
                required: true,
                default: 'Article default title'
            },
            likes: Number,
            isPublished: Boolean
        },
        inheritAttrs: false

    }
</script>

<style scoped>

</style>