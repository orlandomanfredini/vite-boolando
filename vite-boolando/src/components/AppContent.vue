<script>
import CardProduct from './CardProduct.vue';
import storeProducts from '../assets/db 2.json';


export default {

    component: {
        CardProduct,
    },



    data(){
        return {
            products: storeProducts.products,

            

        }
    }
}
</script>

<template>
    <main>
        <div class="container-sm">
            <div class="main-header">
                <h2>Boolando E-commerce</h2>
                <p>Scopri le ultime novità del mese, per te ogni giorno nuovi tantissimi sconti</p>
            </div>
            
            <div class="row row-main">
                <CardProduct v-for="(product, i) in products" :key="i" :singleProduct="product" />
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../assets/scss/content.scss'
</style>