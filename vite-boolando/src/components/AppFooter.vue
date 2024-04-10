<script>
export default {
    data(){
        return{
             company: 'Boolando s.r.l',
             footerLinks: ['Diritti Legali', 'Privacy', 'Impostazione Cookie'],
             link: 'https://fontawesome.com/kits/aa1661fd5d/setup'
            }
        }
}
</script>

<template>
    <footer>
        <h2>{{ company }}</h2>
        <a :href="link" v-for="(link, i) in footerLinks">{{ link }}</a>
    </footer>
</template>

<style lang="scss" scoped>
@use '../assets/scss/footer.scss'
</style>