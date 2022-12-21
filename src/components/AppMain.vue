<script>
import Newsletter from './Newsletter.vue';

export default {
    name: "AppMain",
    components: {
        Newsletter
    }
}
</script>

<template>

    <!-- <section>
        <div>

        </div>
    </section> -->

    <Newsletter />
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

// section {
//     background-image: url(../../public/img/promise-background.jpg);
//     background-position: left center;

//     // debug
//     height: 400px;
// }
</style>