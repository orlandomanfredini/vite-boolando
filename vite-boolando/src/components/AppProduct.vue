<script>
export default {
    props: ['singleProduct'],


    data(){
        return {
            

        }
    },

    methods: {
        calculatePrice(price, discount){
            let result = price - (price * parseInt(discount) / 100) 
            return result.toFixed(2)

        }
    }
    
}
</script>

<template>
<div class="col-4">
    <div class="card">
        <div class="card-img">
            <img :src="singleProduct.frontImage">
            <div  v-for="(info, i) in singleProduct.badges" class="info">
                <div :class="info.type === 'discount' ? 'discount' : 'sustenible' ">{{ info.value }}</div>
            </div>
            
            <div class="overlay">
                <img class="overlay-img" :src="singleProduct.backImage" alt="">
                <div  v-for="(info, i) in singleProduct.badges" class="info">
                    <div :class="info.type === 'discount' ? 'discount' : 'sustenible' ">{{ info.value }}</div>
                </div>
            </div>
        </div>
        <div class="body-card">
            <span>{{ singleProduct.name }}</span>
            <span class="brand">{{ singleProduct.brand }}</span>
            <div class="price">
                <span>{{calculatePrice(singleProduct.price, singleProduct.discount)}}€</span>
                <span class="price-original">{{ singleProduct.price }}€</span>
            </div>
        </div>
    </div>
</div>  
    
</template>

<style lang="scss" scoped>
@use '../assets/scss/card.scss'
</style>