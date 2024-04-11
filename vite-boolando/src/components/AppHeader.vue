<script>
export default {
    data(){
        return{
            currentElement: 0,
            iconsHeader: [
                {
                    icon: '../public/img/cuore.png'
                },
                {
                    icon: '../public/img/carrello.png'
                },
                {
                    icon: '../public/img/log.png'
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
            <div class="row row-header">
                <div class="col-4">
                    <ul class="link-header">
                        <li v-for="link in linksHeader"><a :href="link.src">{{ link.name }}</a></li>
                    </ul>
                </div>
                <div class="logo">
                    <img :src="logo">
                </div>
                <div class="col-4">
                    <ul class="icon-header">
                        <li v-for="(icon, i) in iconsHeader" :key="i">
                            <img :src="icon.icon">
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use './src/assets/scss/header'
</style>