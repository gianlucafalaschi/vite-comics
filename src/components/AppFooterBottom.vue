<script>
export default {
    name: 'AppFooterBottom'
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
                    <div class="icon-box">
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
                    </div>
                    <div class="icon-box">
                        <img src="../assets/img/footer-facebook.png" alt="">
                    </div>
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
}

</style>