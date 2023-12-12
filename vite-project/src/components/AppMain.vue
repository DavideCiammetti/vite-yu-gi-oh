<script>
import axios from 'axios';

     export default{
        name: 'header',
            data(){
            return{
                'cards': [],
                'apiUrl': 'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0',
            };
        },
        created(){
            axios.get(this.apiUrl).then((response)=>{
                this.cards = response.data.results;
            });
        },
    };
   
</script>

<template>
    
</template>

<style scoped lang="scss">
</style>
