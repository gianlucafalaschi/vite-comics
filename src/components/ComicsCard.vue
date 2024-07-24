<script>
export default {
    name: 'ComicsCard',
    props: {
        image: String,
        title: String
    }
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
        height: 250px;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
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
    width: calc(100% / 3);
    }

    .card .image-container {
        height: 280px ;
    }
}

/*----------------
    COLUMNS per MD >= 768px
-----------------*/
@media screen and (min-width: 768px) {

    .card {
    width: calc(100% / 3);
    }

    .card .image-container {
        height: 320px ;
    }
}

/*----------------
    COLUMNS per LG >= 992px
-----------------*/
@media screen and (min-width: 992px) {

    .card {
    width: calc(100% / 4);
    }

    .card .image-container {
        height: 300px ;
    }
}

/*----------------
    COLUMNS per XL >= 1200px
-----------------*/
@media screen and (min-width: 1200px) {
    .card {
    width: calc(100% / 6);
    }

    .card .image-container {
        height: 250px ;
    }
}

/*----------------
    COLUMNS per XXL >= 1400px
-----------------*/
@media screen and (min-width: 1400px) {


    .card .image-container {
        height: 300px ;
    }
}

</style>