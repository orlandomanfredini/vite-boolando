
<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    AppContent,
    AppFooter,
  },
  mounted() {
    console.log("APP.vue")
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