<script>

import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
import SignUp from './components/SignUp.vue'
export default {
  name: "App",
  components: {
    AppHeader,
    AppFooter,
    SignUp
  }
}
</script>

<template>

  <AppHeader />

  <main>

    <SignUp />
    <!-- section courses -->

    <!-- section instructor -->

    <!-- section testimonials -->

    <!-- section latest news -->

    <!-- section newsletter -->
  </main>


  <AppFooter />
</template>

<style lang="scss">
@use './styles/generals.scss' as*;
@use './styles/partials/variables' as*;
</style>
