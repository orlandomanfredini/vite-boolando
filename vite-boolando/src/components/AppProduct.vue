<script>
export default {
    props: ['singleProduct'],


    data(){

        return {

        }
    }
}
</script>

<template>
<div class="col-4">
    <div class="card">
        <div class="card-img">
            <img :src="singleProduct.frontImage">
            <!-- <div class="discount">{{ singleProduct.badges[1].value }} %</div> -->
            <div class="overlay">
                <img class="overlay-img" :src="singleProduct.backImage" alt="">
                <!-- <div class="discount">{{ singleProduct.sconto }} %</div> -->
            </div>
        </div>
        <div class="body-card">
            <span>{{ singleProduct.name }}</span>
            <span class="brand">{{ singleProduct.brand }}</span>
            <div class="price">
                <span>{{ singleProduct.price }}€</span>
                <span class="price-original">{{ singleProduct.price}}€</span>
            </div>
        </div>
    </div>
</div>  
    
</template>

<style lang="scss" scoped>
@use '../assets/scss/card.scss'
</style>