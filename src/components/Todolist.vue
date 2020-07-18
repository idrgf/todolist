<template>
    <div>
        <h2>Liste de tache à faire</h2>

        <form>
            <div class="form-group container">
                <label for="tache">Tache</label>
                <input v-model="formData.tache" class="form-control" type="text" id="tache">
            </div>
            
            <button v-on:click.prevent="create" class="btn btn-primary mb-3">Créer</button>
        </form>

        <ul>
            <li v-bind:key="index" v-for="(tache, index) in tableauTaches" >
                <item v-bind:id="index" :tache="tache" :supprimer="supprimer"></item>
            </li>
        </ul>
        <div class="flex">
            <div class="sas">
                <h3 v-if="counter < 2">{{ counter }} tache à effectuer</h3>
                <h3 v-else>{{ counter }} taches à effectuer</h3>
            </div>
        </div>
    </div>

</template>
<script>
    import Item from './Item'

    export default {
        name: 'todolist',
        data(){
            return{
                formData: {
                    tache:''
                },
                counter: 0,
                tableauTaches: []
            }
        },
        methods: {
            create: function(){
                this.tableauTaches.push(this.formData.tache)
                this.formData.tache = ''
                this.counter ++
            },
            supprimer: function(e) {
                this.tableauTaches.splice(e.target.parentNode.id, 1)
                this.counter --
            }
        },
        components: {
            'item': Item
        }
    }


</script>
<style lang="sass">
li
    list-style: none

    :hover
        background-color: #1bb788

h2
    margin-top: 100px!important

.flex
    height: 100%
    display: flex
    justify-content: center
    align-item : center

    .sas
        width: 40%
        background: #1bb788
        border-radius: 80px

        :hover
            height: 100%
            width: 100%
            background: #0c4735
            border-radius: 80px
        
    
        
    h3
        color: #fff
    
        
        
</style>