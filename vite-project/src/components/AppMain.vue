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
// chimata axios 
    created(){
        axios.get(this.store.apiURL).then((response)=>{
            this.store.itemCard = response.data.data;
            console.log(this.store.itemCard);
        });
    },
};
   
</script>

<template>
    <main id="main">
        <SpeciesList/>

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
