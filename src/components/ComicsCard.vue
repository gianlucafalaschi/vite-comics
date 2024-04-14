<script>
export default {
    name: 'ComicsCard',
    props: ['image', 'title']
}
</script>

<template>
    <div class="card">
        <div class="image-container">
            <img :src="image" alt="">
        </div>
        <div class="title-container">
            <h4 class="title">{{ title }}</h4>
        </div>
    </div>
</template>

<style scoped lang="scss">
/* @use per usare le variabili */
@use '../style/partials/_variables' as *;

.card {
    width: calc((100% / 2));
    padding: 10px;

    .image-container {
        width: 100%;

        img {
            width: 100%;
            
        }
    }
   .title-container {
        margin-top: 10px;
        width: 100%;
        color: $brand-quaternary;

        .title {
            font-size: 16px;
            font-weight: normal;
            word-wrap: break-word;
           
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

    .card {
    width: calc(100% / 4);
    }

}

/*----------------
    COLUMNS per MD >= 768px
-----------------*/

/*----------------
    COLUMNS per LG >= 992px
-----------------*/
@media screen and (min-width: 992px) {

.card {
width: calc(100% / 6);
}

}

</style>