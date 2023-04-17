<template>
   
    <div class="row">
        <CreateCard v-for="(card, index) in store."/>

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