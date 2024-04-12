<script>
import {store} from '../store.js';

export default {
    data(){
        return {
            store: store,

        }
    },

    methods: {
        calculatePrice(price, discount){
            let result = price - (price * parseInt(discount) / 100); 
            return result

        }
    }
    
}
</script>

<template>
<div class="col-4">
    <div class="card">
        <div class="card-img">
            <img :src="store.products.frontImage">
            <div  v-for="(info, i) in store.products" class="info" :key="i">
                <div :class="info.type === 'discount' ? 'discount' : 'sustenible' ">{{ info.value }}</div>
            </div>
            
            <div class="overlay">
                <img class="overlay-img" :src="store.products.backImage" alt="">
                <div  v-for="(info, i) in store.products.badges" class="info" :key="i">
                    <div :class="info.type === 'discount' ? 'discount' : 'sustenible' ">{{ info.value }}</div>
                </div>
            </div>
        </div>
        <div class="body-card">
            <span>{{ store.products.name }}</span>
            <span class="brand">{{ store.products.brand }}</span>
            <div class="price">
                <span>{{calculatePrice(store.products.price, store.products.discount)}}€</span>
                <span class="price-original">{{ store.products.price }}€</span>
            </div>
        </div>
    </div>
</div>  
    
</template>

<style lang="scss" scoped>
@use '../assets/scss/card.scss'
</style>