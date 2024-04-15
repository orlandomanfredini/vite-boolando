<script>
import { store } from '../store';


export default {
    props:{
        open:{
            type: Boolean,
            default: false,
        },
        product : {

        }

        

    },
    data(){
        return{
            store: store.products
        }
    },
    methods: {
        

    },
    mounted(){
        console.log(store);
    }

}
</script>

<template>
    <div v-if="open" class="box-modal">
        <div class="modal">
            <div class="img-box">
                <img :src="product.frontImg" alt="">
            </div>
            <div class="body-product">
                <h2 class="title">
                    {{ product.name }}
                </h2>
                <div class="brand">
                    {{ product.brand }}
                </div>
            </div>
            
            
            
        </div>
    </div>

</template>

<style lang="scss">
.box-modal{
    width: 100%;
    height: 100%;
    position: absolute;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: rgba(white,(0.7));
    z-index: 999;


    .modal{
        width: 800px;
        height: 600px;
        display: flex;
        align-items: center;
        padding: 20px;
        background-color: rgba(orange, 0.5);


        .img-box {


            img{
                max-width: 400px;
                border-radius: 20px;
            }

        }

        .body-product{
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            padding-left: 30px;
            padding-top: 30px;

            .title{
                color: rgb(201, 89, 89);
                margin-bottom: 0;
            }
            

        }
    }
    
}
</style>