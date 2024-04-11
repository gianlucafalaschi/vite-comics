<script>
export default {
    name: 'AppMainOptions'
}
</script>

<template>
    <section id="options-section">
        <div class="container">
            <div class="row">
                <div class="option-box">
                    <div class="image-container">
                        <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                    </div>
                    <div class="description">
                        <div>DIGITAL COMICS</div>
                    </div>
                </div>
                <div class="option-box">
                    <div class="image-container">
                        <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                    </div>
                    <div class="description">
                        <div>DIGITAL COMICS</div>
                    </div>
                </div>
                <div class="option-box">
                    <div class="image-container">
                        <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                    </div>
                    <div class="description">
                        <div>DIGITAL COMICS</div>
                    </div>
                </div>
                <div class="option-box">
                    <div class="image-container">
                        <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                    </div>
                    <div class="description">
                        <div>DIGITAL COMICS</div>
                    </div>
                </div>
                <div class="option-box">
                    <div class="image-container">
                        <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                    </div>
                    <div class="description">
                        <div>DIGITAL COMICS</div>
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
    align-items:center;
    gap: 15px;

    img {
        max-width: 70px;
    }

    .description {
        color: $brand-quaternary;
    }
}


</style>