<template>
    <div class="col-12 col-sm-6 col-md-4">
        <div class="card bg-warning">
            <img :src="c92card.card_images[count].image_url" >
            <h4>{{ c92card.name }}</h4>
            <div class="font-weight-bold">{{ c92card.archetype }}</div>
        </div>

    </div>
</template>

<script>
    export default {
        name: 'CreateCard',
        props: ['c92card'],
        data(){
            return{
                count: 0,
            }
        },
    }
</script>

<style lang="scss" scoped>


</style>