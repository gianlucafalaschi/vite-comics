<script>
import AppHeader from './components/AppHeader.vue';
import AppProducts from './components/AppProducts.vue';
import AppMainOptions from './components/AppMainOptions.vue';

export default {
  components: {
    AppHeader,
    AppProducts,
    AppMainOptions,
  }
}
</script>

<template>
  <AppHeader></AppHeader>
  <main>
    <AppProducts></AppProducts>
    <AppMainOptions></AppMainOptions>
  </main>
</template>

<style lang="scss">
@use './style/generic.scss'
</style>