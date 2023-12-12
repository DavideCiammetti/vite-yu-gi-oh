<script>
import NumberOfCards from './NumberOfCards.vue';
export default{
    name: 'cardsContainer',
        components:{
            NumberOfCards,
        }
}

</script>

<template>
    <NumberOfCards/>
    <div class="cards-container">
        <div class="card">
            <div class="card-img">
                immagine
            </div>
            <div class="info-text">
                <h4><strong>title</strong></h4>
                <p>par</p>
            </div>
        </div>
        <div class="card">
            2
        </div>
        <div class="card">
            3
        </div>
        <div class="card">
            4
        </div>
        <div class="card">
            5
        </div>

        <div class="card">
            1
        </div>
        <div class="card">
            2
        </div>
        <div class="card">
            3
        </div>
        <div class="card">
            4
        </div>
        <div class="card">
            5
        </div>

        <div class="card">
            1
        </div>
        <div class="card">
            2
        </div>
        <div class="card">
            3
        </div>
        <div class="card">
            4
        </div>
        <div class="card">
            5
        </div>

        <div class="card">
            1
        </div>
        <div class="card">
            2
        </div>
        <div class="card">
            3
        </div>
        <div class="card">
            4
        </div>
        <div class="card">
            5
        </div>

    </div>
</template>

<style scoped lang="scss">
@use'../../style/partial/_variables.scss' as *;
  
.cards-container{
    height: 90%;
    border: 1px solid black;
    margin: 0 auto;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 25px;
        .card{
            width: calc((100% / 5) - 20px);
            border: 1px solid black;
            height: 150px;
        }
}
</style>
