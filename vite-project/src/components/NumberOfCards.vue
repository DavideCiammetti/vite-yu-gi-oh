<script>

export default{
    name: 'cardsFound',
}

</script>

<template>
    <div class="cards-found-container">
        <div class="found-content"> 
            <h3>Found 39 cards</h3>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use'../../style/partial/_variables.scss' as *;
    .cards-found-container{
        background-color: #212529;
        margin: 0 auto;
        height: 55px;
            .found-content{
                padding-left: 17px;
                    h3{
                        color: $col-white;
                        line-height: 3;
                    }
            }
    }
</style>
