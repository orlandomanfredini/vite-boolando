<script>
import AppModal from './AppModal.vue';

export default {
    props:['singleProduct'],

    components:{
        AppModal,
    },
    
    data(){
        
        return {
            mondalVisible: false,
            modalObject: {
                name: this.singleProduct.name,
                frontImg: this.singleProduct.frontImage,
                backImg: this.singleProduct.backImage,
                badges: this.singleProduct.badges,
                brand: this.singleProduct.brand,
                price: this.singleProduct.price,
                discount: this.singleProduct.discount,
            }
           

        }
    },
    mounted(){

    },

    methods: {
        calculatePrice(price, discount){
            let result = price - (price * parseInt(discount) / 100); 
            return result.toFixed(2)

        },
        isVisible(){
            this.mondalVisible = true;
        }
        


    }
    
}
</script>

<template>
<div class="col-4" @click="isVisible()">
    <div class="card">
        <div class="card-img">
            <img :src="singleProduct.frontImage">
            <div  v-for="(info, i) in singleProduct.bedges" class="info" :key="i">
                <div :class="info.type === 'discount' ? 'discount' : 'sustenible' ">{{ info.value }}</div>
            </div>
            
            <div class="overlay">
                <img class="overlay-img" :src="singleProduct.backImage" alt="">
                <div  v-for="(info, i) in singleProduct.badges" class="info" :key="i">
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
<AppModal :open="mondalVisible" :product="modalObject"/>
    
</template>

<style lang="scss" scoped>
@use '../assets/scss/card.scss'
</style>