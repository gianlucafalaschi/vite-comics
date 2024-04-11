<script>
export default {
    name: 'AppHeader'
}
</script>

<template>
    <div class="container">
        <div class="logo">
            <img src="../assets/img/dc-logo.png" alt="logo dc">
        </div>

        <nav>
            <ul>
                <li>
                    <a href="#">CHARACTER</a>
                </li>
                <li>
                    <a href="#">COMICS</a>
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
    
</template>

<style scoped lang="scss">
    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
        padding-top:15px;
        padding-bottom:15px;

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
                    a {
                        color: white; 
                    }
                } 
                
            }
        } 
    } 
</style>