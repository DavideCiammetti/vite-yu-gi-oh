<script>
import axios from 'axios';
import {store} from '../store.js';

     export default{
        name: 'main',
            data(){
            return{
                store,
            };
        },
        // chimata axos per prendere dati da api
        created(){
            axios.get(store.apiUrl).then((response)=>{
                store.cards = response.data.results;
            });
        },
    };
   
</script>

<template>
    
</template>

<style scoped lang="scss">
</style>
