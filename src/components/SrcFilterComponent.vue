<template>
    
    <div class="container p-5">
        <label  for="cardArchetype" class="text-uppercase text-dark fw-semibold">Search for archetype</label>
        <select  id="cardArchetype" v-model="store.search.archetype">
            <option  selected value="">Search</option>
            <option :value="archetype">
                {{ archetype }}
            </option>
        </select>
    </div>
   
</template>

<script>
    import {store} from '../data/store';
    import axios from 'axios';
    export default {
        name: 'SrcFilterComponent',
        data(){
            return{
                store,
                statusArchetypes:[],
            }
        },
        methods:{

        },
        mounted(){
            axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php').then((res) => {
            console.log(res.data);
            this.statusArchetypes = res.data;
            })
        }
    }
</script>

<style lang="scss" scoped>

</style>