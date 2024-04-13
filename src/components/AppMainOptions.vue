<script>
export default {
    name: 'AppMainOptions',
    data() {
        return {
            options: [
                
                {   
                    image: 'buy-comics-digital-comics.png',
                    text: 'DIGITAL COMICS',
                    active: false
                },
                {   
                    image: 'buy-comics-merchandise.png',
                    text: 'DC MERCHANDISE',
                    active: false
                },
                {   
                    image: 'buy-comics-subscriptions.png',
                    text: 'SUBSCRIPTION',
                    active: false
                },
                {   
                    image: 'buy-comics-shop-locator.png',
                    text: 'COMIC SHOP LOCATOR',
                    active: false
                },
                {   
                    image: 'buy-dc-power-visa.svg',
                    text: 'DC POWER VISA',
                    active: false
                },
                
            ],
        }
    },
    methods: {   /* Funzione necessaria per far funzionare le immagini dinamiche con VITE */
            getImageUrl(name) {
                return new URL(`../assets/img/${name}`, import.meta.url).href;
            }
    }
}
</script>

<template>
    <section id="options-section">
        <div class="container">
            <div class="row">
                <div v-for="element in options" class="option-box">
                    <div class="image-container">
                        <img :src="getImageUrl(element.image)">
                    </div>
                    <div class="description">
                        <div>{{ element.text }}</div>
                    </div>
                </div> 
            </div> 
        </div>
    </section>  
</template>

<style scoped lang="scss">
/* @use per usare le variabili */
@use '../style/partials/_variables' as *;

#options-section{
    background-color: $brand-primary;

    .container {
        display: flex;
        justify-content: center;
        .row {
            width: 90%;
            padding-top: 30px;
            padding-bottom: 30px;
            margin-left: -10px;
            margin-right: -10px;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-wrap: wrap;
            gap: 15px;
        }
    }
}

.option-box {
    display: flex;
    justify-content: center;
    align-items:center;
    flex-wrap: wrap;
    gap: 15px;
    object-fit: contain;


    img {
        max-width: 70px;
    }

    .description {
        color: $brand-quaternary;
    }
}


</style>