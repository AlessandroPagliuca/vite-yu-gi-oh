<template>
    <header>

        <h1>{{ title }}</h1>

    </header>
</template>

<script>

    export default {
        name: 'HeadeComponent',
        props: {
            title: String,
        },
    }
</script>

<style lang="scss" scoped>

</style>