<template>
  <HeaderComponent title="Yu-Gi-Oh Api"/>
  <main>
    <!--<SrcFilterComponent />-->
  </main>
</template>

<script>
  import { store } from './data/store';
  import axios from 'axios';
  import HeaderComponent from './components/HeaderComponent.vue';
  import SrcFilterComponent from './components/SrcFilterComponent.vue';
  export default {
    name: 'App',
    components:{
      HeaderComponent,
      SrcFilterComponent
    },
    data(){
      return{
        store
      }
    },
    methods:{
      getCards(){
        const url = store.baseUrl;
        axios.get(url).then((res) =>{
          store.cardList = res.data.result;
        })
      }
     
    }
    
  }
</script>

<style lang="scss" scoped>

</style>