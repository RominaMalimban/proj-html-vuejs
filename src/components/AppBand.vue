<script>
export default {
    name: "AppBand"
}
</script>

<template>
    <section>
        <div class="container">
            <div>
                <h2>Start Learning to Drive Today</h2>
                <span>Give us a call to schedule your first driving lesson</span>
            </div>

            <div>
                <i class="fa-solid fa-phone-flip"></i>
                <span>1-800-555-555</span>
            </div>

        </div>

    </section>

</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

section {
    background-image: url(../../public/img/horizontal-cta-background.jpg);
    background-position: center center;
    padding: 70px 0;
    color: #fff;

    .container {
        @include flex(both);

        h2 {
            margin-bottom: 10px;
        }

        i,
        span {
            font-size: 24px;
        }

        i {
            margin-right: 20px;
        }
    }
}
</style>