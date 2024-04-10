<script>
export default {
    data(){
        return{
            iconHeader: [
                {
                    icon: '../'
                }

            ],
            logo: '../public/img/boolean-logo.png',
            linksHeader: [
                {
                    name: 'Uomo',
                    src: 'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter',
                },
                {
                    name: 'Donna',
                    src: 'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter',
                },
                {
                    name: 'Bambino',
                    src: 'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter',
                }
            ]
        }
    }
}
</script>

<template>
    <header>
        <div class="container">
            <div class="row">
                <div class="col-4">
                    <ul class="link-header">
                        <li v-for="link in linksHeader"><a :href="link.src">{{ link.name }}</a></li>
                    </ul>
                </div>
                <div class="col-4">
                    <div class="logo">
                        <img :src="logo">
                    </div>
                </div>
                <div class="col-4">
                    <ul class="icon-header">
                        <li v-for=""></li>
                    </ul>
                </div>
            </div>
        </div>
    </header>
</template>

<style lang="scss">
@use './src/assets/scss/header'
</style>