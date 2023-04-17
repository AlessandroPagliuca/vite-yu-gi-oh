<template>
   <div class="container bg-light">
    <div class="row justify-content-center gap-3">
        <CreateCard v-for="(c92card, index) in store.cardList" :key="c92card.id" :c92card="c92card"/>
    </div>

   </div>

</template>

<script>
import {store} from '../data/store'
import CreateCard from './CreateCard.vue';

    export default {
        name: 'CardsList',
        components:{
            CreateCard,
        },
        data(){
            return{
                store
            }
        },
        methods:{

        }
    }
</script>

<style lang="scss" scoped>

</style>