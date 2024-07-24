<script>
export default {
    name: 'AppFooterBottom',
    data() {
        return {
            socials: [
                
                {   
                    image: 'footer-facebook.png',
                    
                },
                {   
                    image: 'footer-twitter.png',
                    
                },
                {   
                    image: 'footer-youtube.png',
                    
                },
                {   
                    image: 'footer-pinterest.png',
                    
                },
                {   
                    image: 'footer-periscope.png',
                    
                },
               
                
            ],
        }
    },
    methods: {
            getImageUrl(name) {
                return new URL(`../assets/img/${name}`, import.meta.url).href;
            }
    }
}
</script>

<template>
    <section id="footer-bottom">
        <div class="container">
            <div class="sign-up">
                <button class="button button-1" type="button">SIGN-UP NOW!</button>
            </div>
            <div class="socials">
                    <span class="follow">FOLLOW US</span>
                    <div v-for="element in socials" class="icon-box">
                        <img :src="getImageUrl(element.image)" alt="">
                    </div>
                    <!-- <div class="icon-box">
                        <img src="../assets/img/footer-facebook.png" alt="">
                    </div>
                    <div class="icon-box">
                        <img src="../assets/img/footer-facebook.png" alt="">
                    </div>
                    <div class="icon-box">
                        <img src="../assets/img/footer-facebook.png" alt="">
                    </div>
                    <div class="icon-box">
                        <img src="../assets/img/footer-facebook.png" alt="">
                    </div> -->
            </div>
        </div>
    </section>
     
</template>

<style scoped lang="scss">
/* @use per usare le variabili */
@use '../style/partials/_variables' as *;

#footer-bottom {
    width: 100%;
    background-color:#303030;
}

.container {
    padding-top:15px;
    padding-bottom: 15px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;

    .sign-up {
        margin-right: 10px;
    }
    .socials {
        display: flex;
        align-items: center;
        gap: 15px;
        
        

        .icon-box {
            display: flex;
            align-items: center;
        }

        span {
            font-size: 18px;
            color:$brand-primary;
            font-weight: bold;
        }
        
    }

}

.button-1 {
    padding: 8px;
    color: white;
    border: 1px solid $brand-primary; 
    margin-bottom: 5px;
}


/* MEDIA QUERIES */

/*----------------
    COLUMNS per XS > 0px
-----------------*/


/*----------------
    COLUMNS per SM >= 576px
-----------------*/
@media screen and (min-width: 576px) {
    .button-1 {
    margin-bottom: 0px;
    }

}


</style>