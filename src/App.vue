<script>
import AppHeader from './components/AppHeader.vue';
import AppProducts from './components/AppProducts.vue';
import AppMainOptions from './components/AppMainOptions.vue';
import AppFooterLinks from './components/AppFooterLinks.vue';
import AppFooterBottom from './components/AppFooterBottom.vue';

export default {
  components: {
    AppHeader,
    AppProducts,
    AppMainOptions,
    AppFooterLinks,
    AppFooterBottom,
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
    <AppFooterBottom></AppFooterBottom>
  </footer>
</template>

<style lang="scss">
@use './style/generic.scss'
</style>