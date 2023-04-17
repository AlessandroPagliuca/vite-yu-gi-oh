<template>
    <div class="col-12 col-sm-6 col-md-4">
        <div class=" text-center">
            <img :src="c92card.image" :alt="c92card.name">
            <h4>{{ c92card.name }}</h4>
            <div>{{ c92card.status }}</div>
            <div class="font-weight-bold">{{ c92card.species }}</div>
        </div>

    </div>
</template>

<script>
    export default {
        name: 'CreateCard',
        props: ['c92card']
    }
</script>

<style lang="scss" scoped>

</style>