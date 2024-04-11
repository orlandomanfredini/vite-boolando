<script>
import AppProduct from './AppProduct.vue';
import storeProducts from '../assets/db2.json';


export default {

    components: {
        AppProduct,
    },



    data(){
        return {
            products:storeProducts.products,
        }
        
    },
    mounted(){
        console.log(this.products)
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
                <AppProduct v-for="(product, i) in products" :key="i" :singleProduct="product" />
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped >
@use '../assets/scss/content.scss'
</style>./AppProduct.vue