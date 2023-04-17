<template>
  <HeaderComponent title="Yu-Gi-Oh Api"/>
  <main>
    <!--<SrcFilterComponent />-->
    <CardsList />
  </main>
</template>

<script>
  import { store } from './data/store';
  import axios from 'axios';
  import HeaderComponent from './components/HeaderComponent.vue';
  import SrcFilterComponent from './components/SrcFilterComponent.vue';
  import CardsList from './components/CardsList.vue';
  export default {
    name: 'App',
    components:{
      HeaderComponent,
      CardsList,
      SrcFilterComponent
    },
    data(){
      return{
        store
      }
    },
    methods:{
      getCards(){
        const url = store.baseUrl + store.endpoint;
        axios.get(url).then((res) =>{
          store.cardList = res.data.data;
        })

      }
     
    },
    mounted() {
      store.endpoint = 'name';
    this.getCards();
   }
      
  }
</script>

<style lang="scss" scoped>

</style>