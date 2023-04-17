<template>
    <div class="col-12 col-sm-6 col-md-4 col-lg-3 col-xl-2">
        <div class="card bg-warning" >
            <img class="card-img-top" :src="c92card.card_images[count].image_url" >
            <div class="card-body text-center">
                <h4 class="card-title">{{ c92card.name }}</h4>
                <div class="font-weight-bold card-text">{{ c92card.archetype }}</div>
            </div>
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