<script>

import AppNavbar from './AppNavbar.vue';

export default {
    name: "AppHeader",
    components: {
        AppNavbar
    }
}

</script>

<template>

    <header>
        <!-- header top -->
        <div class="top-header">
            <div class="container">
                <div>We have a 95&percnt; Succesfull Pass Rate!</div>
                <div>
                    <i class="fa-solid fa-phone-flip"></i>
                    Give us a call to book your tuition! 1-800-555-555
                </div>
            </div>
        </div>
        <!-- chiusura top header -->

        <!-- sub-header -->
        <div class="sub-header">

            <!-- componente navbar -->
            <AppNavbar />

            <div class="container">
                <h1>Drive with Avada</h1>
                <h3>We offer the finest driving tuition money can buy</h3>
            </div>

            <div class="stickers">
                <div class="sticker">
                    <i class="fa-solid fa-book"></i>
                    <span class="txt-sticker">Demos</span>
                </div>
                <div class="sticker">
                    <div>
                        <strong><span class="green dollar">&dollar;</span></strong>
                        <strong><span class="green number">39</span></strong>
                    </div>
                    <span class="txt-sticker">On Sale</span>
                </div>
            </div>

        </div>
        <!-- chiusura sub-header -->
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

// regole top header
.top-header {
    height: 40px;
    width: 100%;
    background-color: $bg-gray;
    font-size: $small-font;

    .container {
        height: 100%;
        @include flex(both);
        color: $navy;
        font-weight: bold;

        i {
            padding-right: 10px;
        }
    }
}

// regole sub-header
.sub-header {
    height: 720px;
    background-image: url(/img/homepage-hero-background.jpg);
    background-size: cover;
    position: relative;
    @include flex (center);

    h1,
    h3 {
        color: $white;
    }

    h1 {
        font-size: 40px;
        padding-bottom: 10px;
    }

    .stickers {
        position: absolute;
        right: 15px;
        top: 110px;

        .sticker {
            text-align: center;
            padding: 5px;
            background-color: #fff;
            margin-bottom: 10px;
            border-radius: 10px;
            position: relative;

            i {
                color: #33475b;
            }

            .green {
                color: $primary;
                font-weight: bolder;

                &.dollar {
                    font-size: 11px;
                    position: absolute;
                    top: 5px;
                    left: 7px;
                }

                &.number {
                    font-size: 18px;
                }
            }

            .txt-sticker {
                display: block;
                color: #33475b;
                font-size: $small-font;
                padding-top: 5px;
            }
        }

    }
}
</style>