<template>
    <div class="card my-2 item-todo container">
        <p>{{ tache }}</p>
        <div v-on:click="supprimer" class="btn-supr btn-danger"><i class="fa fa-times"></i></div>
    </div>

</template>
<script>
export default {
    name: 'Item',
    props: ['tache', 'supprimer']
}


</script>
<style lang="sass">
.item-todo
    position: relative
    padding: 20px 60px 20px 30px
    font-size: 20px
    height: 88px

.btn-supr
    position: absolute
    border-radius: 10px
    width: 30px
    right: 10px
    top: 30px

    &:hover
        cursor: pointer




</style>