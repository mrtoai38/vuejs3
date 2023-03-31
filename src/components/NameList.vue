<template>
    <div>
        <h3 v-for="name in names" :key="name.firstName">
            {{ name.firstName }} {{ name.lastName }}
        </h3>
    </div>
</template>

<script>
    export default {
        name: 'NameList',
        data() {
            return {
                names: [
                    {
                        firstName: 'Bruce',
                        lastName: 'Wayne'
                    },
                    {
                        firstName: 'Clark',
                        lastName: 'Kent'
                    },
                    {
                        firstName: 'Princess',
                        lastName: 'Diana'
                    },
                ]
            }
        }
    }
</script>

<style scoped>

</style>