<script>
import AppHeader from './components/AppHeader.vue';
import AppBanner from './components/AppBanner.vue';
export default {
  data() {
    return {

    }
  },
  components: {
    AppHeader,
    AppBanner,
  },
}
</script>

<template>
  <AppHeader />
  <section>
    <AppBanner />
  </section>

</template>

<style lang="scss">
@use "./styles/general.scss" as*;
@use "./styles/partials/variables" as*;

section {
  background-color: $color-current-slide;
}
</style>
