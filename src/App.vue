<script>

import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  name: "App",
  components: {
    AppHeader,
    AppFooter
  }
}
</script>

<template>

  <AppHeader />

  <main>
    <!-- section request callback -->

    <!-- section courses -->

    <!-- section instructor -->

    <!-- section testimonials -->

    <!-- section latest news -->

    <!-- section newsletter -->
  </main>

  <!-- footer -->
  <AppFooter />
</template>

<style lang="scss">
@use './styles/generals.scss' as*;
@use './styles/partials/variables' as*;
</style>
