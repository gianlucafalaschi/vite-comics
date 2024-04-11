<script>
export default {
    name: 'AppProducts'
}
</script>

<template>
    <section id="products-section">
        <div class="container">
            <h3>-->Content goes here<--</h3>
        </div>
    </section>
     
</template>

<style scoped lang="scss">
/* @use per usare le variabili */
@use '../style/partials/_variables' as *;

#products-section {
    width: 100%;
    min-height: 50px;  /* TODO remove the min height */
    background-color: $brand-secondary;
    

    .container {
        background-color: transparent;
        padding-top:30px;
        padding-bottom:30px;
    } h3 {
        color: white;
    } 
} 
</style>