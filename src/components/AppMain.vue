<script>
import Newsletter from './Newsletter.vue';
import Testimonials from './Testimonials.vue';
import LatestNewsVue from './LatestNews.vue';

export default {
    name: "AppMain",
    components: {
        Newsletter,
        Testimonials,
        LatestNews
    }
}
</script>

<template>

    <Testimonials />
    <LatestNews />
    <Newsletter />
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;
</style>