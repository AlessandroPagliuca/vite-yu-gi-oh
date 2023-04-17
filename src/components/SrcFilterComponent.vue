<template>
    
    <div class="container p-5">
        <select name="" id="">
            <option value="option.archetype" selected>Alien</option>
        </select>
    </div>
   
</template>

<script>
    export default {
        name: 'SrcFilterComponent',
        data(){
            return{
                props:['option']
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>