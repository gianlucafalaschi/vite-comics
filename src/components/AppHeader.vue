<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            links: [
                
                {
                    text: 'CHARACTER',
                    active: false
                },
                {
                    text: 'COMICS',
                    active: true
                },
                {
                    text: 'MOVIES',
                    active: false
                },
                {
                    text: 'TV',
                    active: false
                },
                {
                    text: 'GAMES',
                    active: false
                },
                {
                    text: 'COLLECTIBLES',
                    active: false
                },
                {
                    text: 'VIDEOS',
                    active: false
                },
                {
                    text: 'FANS',
                    active: false
                },
                {
                    text: 'NEWS',
                    active: false
                },
                {
                    text: 'SHOP',
                    active: false
                },
            ],
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
                    <li :class="{'active': element.active}" v-for="element in links">
                        <a :class="{'active': element.active}" href="#">{{element.text}}</a>
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
        /* padding-top:15px;
        padding-bottom:15px; */
        background-color: $brand-quaternary;
        border: 1px dashed gray;

        .logo {
            width: 20%;
            img {
                max-width: 100px;
            }
        }

        nav{
            width: 80%;
            ul {
                width: 100%;
                display: flex;
                justify-content: flex-end;
                flex-wrap: wrap;
                gap: 20px;
                font-size: 16px;
                li {
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
</style>