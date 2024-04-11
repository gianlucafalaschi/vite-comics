<script>
export default {
    name: 'AppHeader'
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
                    <li>
                        <a href="#">CHARACTER</a>
                    </li>
                    <li class="active">
                        <a class="active" href="#">COMICS</a>
                    </li>
                    <li>
                        <a href="#">MOVIES</a>
                    </li>
                    <li>
                        <a href="#">TV</a>
                    </li>
                    <li>
                        <a href="#">GAMES</a>
                    </li>
                    <li>
                        <a href="#">CHARACTER</a>
                    </li>
                    <li>
                        <a href="#">CHARACTER</a>
                    </li>
                    <li>
                        <a href="#">CHARACTER</a>
                    </li>
                    <li>
                        <a href="#">CHARACTER</a>
                    </li>
                    <li>
                        <a href="#">CHARACTER</a>
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
        padding-top:15px;
        padding-bottom:15px;
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
                    padding-top: 20px;
                    padding-bottom: 20px;
                    &.active {
                        border-bottom: 3px solid $brand-primary;
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