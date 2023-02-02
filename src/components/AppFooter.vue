<script>
import AppFooterBuy from './AppFooterBuy.vue';
import AppFooterLinks from './AppFooterLinks.vue';
import AppFooterFooter from './AppFooterFooter.vue';

export default {
      name: 'AppFooter',
      components: {
            AppFooterBuy,
            AppFooterLinks,
            AppFooterFooter
      }
}
</script>

<template>

      <footer>
            <AppFooterBuy />

            <AppFooterLinks />

            <AppFooterFooter />
      </footer>

</template>

<style lang="scss" scoped>

</style>