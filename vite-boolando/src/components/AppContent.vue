<script>
import AppProduct from './AppProduct.vue';
import AppModal from './AppModal.vue';
import {store} from '../store.js'


export default {

    components: {
        AppProduct,
        AppModal,
    },
    data(){
        return {
            store : store,
            isVisibleModal : false,
            
        }
    },
    methods:{
        visibleModal(){
           this.isVisibleModal = true;
        }
    },
    mounted(){
        console.log(this.store)
        
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
                <AppProduct v-for="(product, i) in store.products" :key="i" :singleProduct="product" />
                
            </div>
            
        </div>
    </main>
</template>

<style lang="scss" scoped >
@use '../assets/scss/content.scss'

</style>