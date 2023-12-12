<script>
import axios from 'axios';
import {store} from '../store.js';
import CardsContainer from './CardsContainer.vue';
import SpeciesList from './SpeciesList.vue';

     export default{
        name: 'main',
            components:{
                CardsContainer,
                SpeciesList,
            },

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
    <main id="main">
        <SpeciesList/>
        <div class="main-container">
            <CardsContainer/>
        </div>
    </main>
</template>

<style scoped lang="scss">
@use'../../style/partial/_variables.scss' as *;

    #main{
        background-color: $bg-orange-main;
        .main-container{
        background-color: $col-white;
        width: 85%;
        padding: 48px;
        margin: 0 auto;
        }
    }
</style>
