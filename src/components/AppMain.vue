<script>
import Newsletter from './Newsletter.vue';
import Testimonials from './Testimonials.vue'

export default {
    name: "AppMain",
    components: {
        Newsletter,
        Testimonials
    }
}
</script>

<template>

    <!-- <section>
        <div>

        </div>
    </section> -->
    <Testimonials />
    <Newsletter />
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

// section {
//     background-image: url(/img/promise-background.jpg);
//     background-position: left center;

//     // debug
//     height: 400px;
// }
</style>