<script>
export default {
    name: 'ComicsCard',
}
</script>

<template>
    <div class="card">
        <div class="image-container">
            <img src="https://www.coverbrowser.com/image/action-comics/1-1.jpg" alt="">
        </div>
        <div class="title-container">
            <h4 class="title">Batman: White Knight Presents: Harley Quinn</h4>
        </div>
    </div>
</template>

<style scoped lang="scss">
/* @use per usare le variabili */
@use '../style/partials/_variables' as *;

.card {
    width: calc((100% / 6));
    padding: 10px;
    border: 1px dashed red;

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
           
        }
   } 
}   



</style>