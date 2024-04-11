<script>
import AppHeader from './components/AppHeader.vue';
import AppProducts from './components/AppProducts.vue';

export default {
  components: {
    AppHeader,
    AppProducts,
  }
}
</script>

<template>
  <AppHeader></AppHeader>
  <main>
    <AppProducts></AppProducts>
  </main>
</template>

<style lang="scss">
@use './style/generic.scss'
</style>