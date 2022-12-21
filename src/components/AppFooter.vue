<script>
export default {
    name: "AppFooter"
}
</script>

<template>

    <footer>
        <!-- top-footer -->
        <div class="top-footer">

        </div>

        <!-- sub-footer -->
        <div class="sub-footer">
            <div class="container">
                &copy; Copyright 2 012 - 2020 | Avada Theme by <span>ThemeFusion</span> | All Rights Reserved | Powered
                by <span>Wordpress</span>
            </div>
        </div>
    </footer>

</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

.top-footer {
    background-image: url(../../public/img/footer-background-color.jpg);
    // debug
    height: 300px;
}

.sub-footer {
    background-color: #1c1d1e;

    .container {
        padding: 60px 0;
        font-size: $small-font;
        color: #676360;

        span {
            color: $primary;
        }
    }
}
</style>
