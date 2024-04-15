
<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';
import AppFooter from './components/AppFooter.vue';
import axios from 'axios';
import {store} from './store.js';

export default {
  components: {
    AppHeader,
    AppContent,
    AppFooter,
  },
  methods:{
    storeProducts(){
      axios.get('http://localhost:3000/products')
      .then((res)=>{
        console.log(res.data);
        store.products = res.data;
      })
    }
  },
  mounted() {
    this.storeProducts()
    
  }
}
</script>



<template>
  <AppHeader />
  <AppContent />
  <AppFooter />
</template>

<style lang="scss">
body{
  font-family: "Roboto", sans-serif;
}

</style>