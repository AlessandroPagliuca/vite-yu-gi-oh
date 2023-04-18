<template>
   <div class="container bg-light">
   
    <div class="row justify-content-center gap-3">
         <!--counter delle carte visualizzate in pagina-->
        <CounterComponent />
        <CreateCard v-for="c92card in store.cardList" :c92card="c92card"/>
    </div>

   </div>

</template>

<script>
import { store } from '../data/store'
import CreateCard from './CreateCard.vue';
import CounterComponent from './CounterComponent.vue';
    export default {
        name: 'CardsList',
        components:{
            CreateCard,
            CounterComponent,
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