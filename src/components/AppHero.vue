<script>
    export default {
    name: 'AppHero',
}
</script>

<template>
    <section id="hero">
        <div class="hero-image-container"></div>
    </section>
</template>

<style scoped lang="scss">
/* @use per usare le variabili */
@use '../style/partials/_variables' as *;


.hero-image-container {
    width: 100%;
    height: 400px;
    background-image: url('../assets/img/jumbotron.jpg');
    background-position:  top;
    object-fit: contain;
} ;

</style>