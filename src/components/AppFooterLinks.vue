<script>
export default {
    name: 'AppFooterLinks'
}
</script>

<template>
    <section id="footer-map">
        <div class="container">
            <div class="row">
                <div class="col-50-left">
                    <div class="col">
                        <div class="links-box">
                            <div class="links-title">
                                DC COMICS
                            </div>
                            <ul class="links-list">
                                <li>Character</li>
                                <li>Character</li>
                                <li>Character</li>
                                <li>Character</li>
                                <li>Character</li>
                                <li>Character</li>
                                <li>Character</li>
                            </ul>
                        </div>
                    </div>
                    <div class="col">
                        <div class="links-box">
                            <div class="links-title">
                                DC COMICS
                            </div>
                            <ul class="links-list">
                                <li>Character</li>
                                <li>Character</li>
                                <li>Character</li>
                                <li>Character</li>
                                <li>Character</li>
                                <li>Character</li>
                                <li>Character</li>
                            </ul>
                        </div>
                    </div>
                    <div class="col">
                        <div class="links-box">
                            <div class="links-title">
                                DC COMICS
                            </div>
                            <ul class="links-list">
                                <li>Character</li>
                                <li>Character</li>
                                <li>Character</li>
                                <li>Character</li>
                                <li>Character</li>
                                <li>Character</li>
                                <li>Character</li>
                            </ul>
                        </div>
                    </div>
                    <div class="col">
                        <div class="links-box">
                            <div class="links-title">
                                SHOPS
                            </div>
                            <ul class="links-list">
                                <li>Character</li>
                                <li>Character</li>
                            </ul>
                        </div>
                    </div>
                </div>
                    
                <div class="col-50-right">
                    <div class="big-logo-container">
                        <img src="../assets/img/dc-logo-bg.png" alt="">
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

    .row {
        width: 100%;
        height: 100%;
        margin-left: -10px;
        margin-right: -10px;
        display: flex;
        padding-top: 30px;
        padding-bottom: 30px;

        .col {
            
            border: 1px dashed white;
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

.col-50-left {
    width: 50%;
    display: flex;
    flex-wrap: wrap;
}

.col-50-right {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    width: 50%;
    color: white;
    

    .big-logo-container {
        margin: -60px 0;

        img {
            height: 100%;
           
        }

    }

}



</style>