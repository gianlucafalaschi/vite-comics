<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            links: [
                
                {
                    text: 'CHARACTER',
                },
                {
                    text: 'COMICS',
                },
                {
                    text: 'MOVIES',
                    
                },
                {
                    text: 'TV',
                    
                },
                {
                    text: 'GAMES',
                    
                },
                {
                    text: 'COLLECTIBLES',
                    
                },
                {
                    text: 'VIDEOS',
                    
                },
                {
                    text: 'FANS',
                    
                },
                {
                    text: 'NEWS',
                    
                },
                {
                    text: 'SHOP',
                    
                },
            ],
            activeLink: 1,
        }
    },
    methods: {
        elementIsActive: function (index){
            this.activeLink = index;
        }
    }
}
</script>

<template>
    <header>
        <div class="container">
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="logo dc">
            </div>

            <nav>
                <ul>
                    <li v-for="(element, index) in links" :class="{'active' : index == activeLink}" @click="elementIsActive(index)">
                        <a :class="{'active': index == activeLink}" href="#">{{element.text}}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header> 
</template>

<style scoped lang="scss">
/* @use per usare le variabili */
@use '../style/partials/_variables' as *;

    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
        background-color: $brand-quaternary;

        .logo {
            width: 20%;
            padding:10px 10px 10px 0;

            img {
                max-width: 100px;
            }
        }

        nav{
            width: 65%;
            ul {
                width: 100%;
                display: flex;
                flex-wrap: wrap;
                gap: 20px;
                font-size: 16px;
                li {
                    height: 22px;
                    display: flex;
                    align-items: center;
                    position: relative;

                    &.active::after {
                        content: '';
                        width: 100%;
                        height: 4px;
                        background-color:$brand-primary ;
                        position: absolute;
                        left: 0;
                        bottom: 0;
                    }
                    
                    a {
                        color:$brand-tertiary; 
                        &.active {
                            color:$brand-primary;
                        }
                    }
                    
                } 
                
            }
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
    .container nav {
        width: 75%;
    }

}

/*----------------
COLUMNS per MD >= 768px
-----------------*/
@media screen and (min-width: 768px) {
    .container nav {
        width: 80%;
    }

}


</style>