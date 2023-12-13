<script>
import { store } from '../store';

export default{
    name: 'specis',

    data(){
           return{
            store,
           };
        },
}

</script>

<template>
    <div class="species-list-container">
        <select name="specie" id="cars" class="specie" @click="$emit('search')" v-model="store.searchWord">
            <option v-for="types in this.store.type" :value="types.archetype_name"> {{types.archetype_name}}</option>
        </select>
    </div>
</template>

<style scoped lang="scss">
@use'../../style/partial/_variables.scss' as *;

    .specie{
        border: none;
        padding: 10px 90px 10px 10px;
        margin-left: 8%;
        margin-top: 24px;
        margin-bottom: 24px;
        border-radius: 7px;
        border: 1px solid rgb(169, 169, 169);
    }
</style>
