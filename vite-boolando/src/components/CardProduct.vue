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
            <img :src="singleProduct.frontimg">
            <div class="discount">{{ singleProduct.badges[1].value }} %</div>
            <div class="overlay">
                <img class="overlay-img" :src="product.overlayImg" alt="">
                <div class="discount">{{ product.sconto }} %</div>
            </div>
        </div>
        <div class="body-card">
            <span>{{ product.nome }}</span>
            <span class="brand">{{ product.modello }}</span>
            <div class="price">
                <span>{{ product.prezzoScontato.toFixed(2) }}€</span>
                <span class="price-original">{{ product.prezzo.toFixed(2) }}€</span>
            </div>
        </div>
    </div>
</div>  
    
</template>