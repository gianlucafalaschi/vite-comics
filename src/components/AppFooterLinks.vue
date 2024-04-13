<script>
export default {
    name: 'AppFooterLinks',
    data() {
        return {
            columns: [
                {   
                    title: 'DC COMICS',
                    links: [
                        'Characters',
                        'Comics',
                        'Movies',
                        'TV',
                        'Games',
                        'Video',
                        'News',
                    ],    
                },
                {   
                    title: 'DC',
                    links: [
                        'Terms Of Use',
                        'Privacy Policy(New)',
                        'Add Choiches',
                        'Advertising',
                        'Jobs',
                        'Subscription',
                        'Talent Workshop',
                        'CPSC Certificates',
                        'Ratings',
                        'Shop Helps',
                        'Contact Us',
                    ],     
                },
                {   
                    title: 'SITES',
                    links: [
                        'DC',
                        'MAD Magazine',
                        'DC Kids',
                        'DC Universe',
                        'DC Power Visa',
                    ],    
                },
                {   
                    title: 'SHOPS',
                    links: [
                        'Shop DC',
                        'Shop DC Collectables',
                        'DC Kids',
                        'DC Universe',
                        'DC Power Visa',
                    ],   
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
    <section id="footer-map">
        <div class="container">
            <div class="row">
                <div class="col-50-left">
                    <div v-for="column in columns" class="col-links">
                        <div class="links-box">
                            <div class="links-title">
                                {{ column.title }}
                            </div>
                            <ul v-for="link in column.links" class="links-list">
                                <li>{{link}}</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>  
</template>

<style scoped lang="scss">
/* @use per usare le variabili */
@use '../style/partials/_variables' as *;

#footer-map {
    width: 100%;
    background-image: url('../assets/img/footer-bg.jpg');

    .container {
        background-image: url('../assets/img/dc-logo-bg.png');
        background-repeat: no-repeat;
        background-position: 100%;

    

        .row {
            width: 100%;
            height: 100%;
            margin-left: -10px;
            margin-right: -10px;
            display: flex;
            padding-top: 30px;
            padding-bottom: 30px;

            .col-links {
                
                color: $brand-quaternary;
                padding: 0 10px;

                .links-title {
                    color:$brand-quaternary ;
                    margin-bottom: 10px;
                    font-size: 18px;
                }
                .links-list {
                    color: $brand-tertiary;
                    
                    li {
                        margin: 5px 0;
                        font-size: 14px;
                    }
                }
            }
        }
    }    
} 

.col-50-left {
    width: 50%;
    display: flex;
    flex-wrap: wrap;
}

.col-50-right {
    width: 50%;
}



</style>