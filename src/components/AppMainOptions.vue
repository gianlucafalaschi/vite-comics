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
                        {{ element.text }}
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
            flex-wrap: wrap;
            justify-content: center;
            align-items: center;
            gap: 15px;
        }
    }
}

.option-box {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items:center;
    flex-wrap: wrap;
    gap: 15px;

    .image-container {
        width: 100%;
        height: 100px;
        display: flex;
        justify-content: center;

        
        img {
        max-width: 100%;
        height: 100%;
        object-fit: cover;

        }
        
    }

    .description {
        color: $brand-quaternary;
        text-align: center;
    }
    

    
}

/* MEDIA QUERIES */

/*----------------
    COLUMNS per XS > 0px
-----------------*/


/*----------------
    COLUMNS per SM >= 576px
-----------------*/
@media screen and (min-width: 576px) {
    .option-box {
        width: calc(50% - 15px);
    }

}

/*----------------
COLUMNS per MD >= 768px
-----------------*/
@media screen and (min-width: 768px) {
    .option-box {
        width: calc(25% - 15px);
    }

}

/*----------------
COLUMNS per LG >= 992px
-----------------*/
@media screen and (min-width: 992px) {
    

}

/*----------------
COLUMNS per XL >= 1200px
-----------------*/
@media screen and (min-width: 1200px) {

}

/*----------------
COLUMNS per XXL >= 1400px
-----------------*/
@media screen and (min-width: 1400px) {



}
</style>