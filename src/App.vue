<script>

import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
import SignUp from './components/SignUp.vue';
import AppBand from './components/AppBand.vue';
import AppMain from './components/AppMain.vue'

export default {
  name: "App",
  components: {
    AppHeader,
    AppFooter,
    SignUp,
    AppBand,
    AppMain
  }
}
</script>

<template>
  <AppHeader />
  <SignUp />
  <AppBand />
  <AppMain />
  <AppFooter />
</template>

<style lang="scss">
@use './styles/generals.scss' as*;
@use './styles/partials/variables' as*;
</style>
