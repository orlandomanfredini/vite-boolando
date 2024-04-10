<script>
export default {
    data(){
        return {
            products: [
                {
                    nome: 'T-shirt estiva',
                    prezzo: 29.90,
                    prezzoScontato: 20.90,
                    sconto: 30,
                    modello: 'Levis',
                    img: '../public/img/1.webp'

                },
                {
                    nome: 'T-shirt UOMO',
                    prezzo: 39.90,
                    prezzoScontato: 30.90,
                    sconto: 50,
                    modello: 'Tevis',
                    img: '../public/img/2.webp'

                },
                {
                    nome: 'T-shirt estiva',
                    prezzo: 29.90,
                    prezzoScontato: 20.90,
                    sconto: 30,
                    modello: 'Levis',
                    img: '../public/img/3.webp'

                },
                {
                    nome: 'T-shirt estiva',
                    prezzo: 29.90,
                    prezzoScontato: 20.90,
                    sconto: 30,
                    modello: 'Levis',
                    img: '../public/img/4.webp'

                },
                {
                    nome: 'T-shirt estiva',
                    prezzo: 29.90,
                    prezzoScontato: 20.90,
                    sconto: 30,
                    modello: 'Levis',
                    img: '../public/img/5.webp'

                },
                {
                    nome: 'T-shirt estiva',
                    prezzo: 29.90,
                    prezzoScontato: 20.90,
                    sconto: 30,
                    modello: 'Levis',
                    img: '../public/img/6.webp'

                },
            ]

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
            
            <div class="row">
                <div class="col-4">
                    <div class="card"></div>
                </div>
                
            </div>
        </div>
    </main>
</template>

<style lang="scss">
@use '../assets/scss/content.scss'
</style>