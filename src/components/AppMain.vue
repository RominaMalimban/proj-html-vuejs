<script>
import Newsletter from './Newsletter.vue';
import Testimonials from './Testimonials.vue';
import LatestNews from './LatestNews.vue';
import Instructors from './Instructors.vue';
import Rate from './Rate.vue';

export default {
    name: "AppMain",
    components: {
        Newsletter,
        Testimonials,
        LatestNews,
        Instructors,
        Rate
    }
}
</script>

<template>
    <Rate />
    <Instructors />
    <Testimonials />
    <LatestNews />
    <Newsletter />
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;
</style>