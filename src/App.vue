<script>
import AppHeader from './components/AppHeader.vue';
import AppBanner from './components/AppBanner.vue';
import AppMarket from './components/AppMarket.vue';

export default {
  data() {
    return {

    }
  },
  components: {
    AppHeader,
    AppBanner,
    AppMarket,
  },
}
</script>

<template>
  <AppHeader />
  <section>
    <AppBanner />
  </section>
  <section class="market-section">
    <AppMarket />
  </section>

</template>

<style lang="scss">
@use "./styles/general.scss" as*;
@use "./styles/partials/variables" as*;

section {
  background-color: $color-current-slide;
}

.market-section {
  background-color: $color-primary;
}
</style>
