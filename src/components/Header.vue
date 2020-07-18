<template>
    <div>
        <h1>{{ head }}</h1>
    </div>

</template>
<script>
    export default {
        name: 'Header',
        data(){
            return{
                head: 'Ma todolist'
            }
        }
    }


</script>
<style lang="sass" scoped>
div
    position: fixed
    top:0
    width: 100%
    text-align: center
    background-color: #0c4735

    h1
        color: #fff
        heigth:50px
        line-height: 50px

</style>