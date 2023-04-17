<template>
    <div class="col-12 bg-dark">
        <p class="text-white fw-semibold">Found <span>{{ count }}</span> cards</p>
    </div>
</template>

<script>
    export default {
        name: 'Counter',
        data(){
            return{
                count: 0,
            }
        },
        methods:{
         
        }
    }
</script>

<style lang="scss" scoped>

</style>