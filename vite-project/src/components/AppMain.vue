<script>
import axios from 'axios';
import { store } from '../store';
import SpeciesList from './SpeciesList.vue';
import CardsContainer from './CardsContainer.vue';

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
    methods:{
    
        newSearch(){
            axios.get(this.store.apiURL + '?archetype=' + this.store.searchWord).then((response)=>{
                this.store.itemCard = response.data.data;
            });

        axios.get(this.store.archetypeUrl).then((response)=>{
            this.store.type = response.data;
            console.log('sono search ' + this.store.searchWord);
        });
        }

    },
// chimata axios 
    created(){
        this.newSearch();
    },
};
   
</script>

<template>
    <main id="main">
        <!-- ricerca carte per tipo -->
        <SpeciesList @search=" newSearch"/>

        <!-- struttura a 2 main per ilclusione delle singole carte che avviene nel file //CardsContainer// -->
        <CardsContainer 
        :itemCard = "this.store.itemCard"

        />
    </main>
</template>

<style scoped lang="scss">
@use'../../style/partial/_variables.scss' as *;

    #main{
        background-color: $bg-orange-main;
    }
</style>
