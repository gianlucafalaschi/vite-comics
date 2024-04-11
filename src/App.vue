<script>
import AppHeader from './components/AppHeader.vue';
import AppProducts from './components/AppProducts.vue';
import AppMainOptions from './components/AppMainOptions.vue';
import AppFooterLinks from './components/AppFooterLinks.vue';

export default {
  components: {
    AppHeader,
    AppProducts,
    AppMainOptions,
    AppFooterLinks,
  }
}
</script>

<template>
  <AppHeader></AppHeader>
  <main>
    <AppProducts></AppProducts>
    <AppMainOptions></AppMainOptions>
  </main>
  <footer>
    <AppFooterLinks></AppFooterLinks>
  </footer>
</template>

<style lang="scss">
@use './style/generic.scss'
</style>