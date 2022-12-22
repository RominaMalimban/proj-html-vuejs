<script>

export default {
    name: "AppHeader",
    data() {
        return {
            title: "Drive with Avada",
            logo: "img/avada-drivers-logo-2x-300x58.png",
            links: [
                {
                    text: "HOME",
                    url: "#",
                    current: true
                },
                {
                    text: "ABOUT",
                    url: "#",
                    current: false
                },
                {
                    text: "PRICES",
                    url: "#",
                    current: false
                },
                {
                    text: "COURSES",
                    url: "#",
                    current: false,
                    label: "NEW"
                },
                {
                    text: "HOME",
                    url: "#",
                    current: false
                },
                {
                    text: "LOCATIONS",
                    url: "#",
                    current: false
                },
                {
                    text: "BLOG",
                    url: "#",
                    current: false
                }
            ]
        }
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

        <!-- sub-header -->
        <div class="sub-header">

            <!-- nav bar -->
            <nav>
                <div class="container">
                    <a href="#">
                        <img :src="logo" alt="logo">
                    </a>

                    <div class="dx">
                        <ul>
                            <li v-for="(link, index) in links" :key="index">
                                <a :href="link.url" :class="{ active: link.current }">{{ link.text }}</a>
                                <span v-if="link.label" class="new-label">{{ link.label }}</span>
                            </li>

                        </ul>

                        <a href="#" class="btn">BOOK NOW</a>
                    </div>

                </div>
            </nav>
            <!-- chiusura nav bar -->

            <div class="container">
                <h1>{{ title }}</h1>
                <h3>We offer the finest driving tuition money can buy</h3>
            </div>

            <div class="stickers">
                <div>
                    <i class="fa-solid fa-book"></i>
                    <span class="txt-sticker">Demos</span>
                </div>
                <div>
                    <span class="green">&dollar; 39</span>
                    <span class="txt-sticker">On Sale</span>
                </div>
            </div>

        </div>
        <!-- header bottom -->
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

.top-header {
    height: 40px;
    width: 100%;
    background-color: #353637;
    font-size: $small-font;

    .container {
        height: 100%;
        @include flex(both);
        color: $light-grey;

        i {
            padding-right: 10px;
        }
    }
}

.sub-header {
    height: 720px;
    background-image: url(/img/homepage-hero-background.jpg);
    background-size: cover;
    position: relative;
    @include flex (center);

    nav {
        padding: 30px 0;
        background-color: #666b6684;
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;

        .container {
            // height: 100%;
            @include flex(both);

            .dx {
                @include flex(both)
            }

            ul {
                @include flex(both);

                li {
                    padding-left: 30px;

                    a {
                        color: #fff;
                        font-size: 14px;
                        font-weight: bold;

                        &.active {
                            color: $primary;
                            border-bottom: 3px solid $primary;
                        }
                    }

                    .new-label {
                        color: white;
                        font-size: 12px;
                        margin-left: 5px;
                        background-color: $primary;
                        padding: 3px 5px;
                        border-radius: 3px;
                        font-weight: bold;
                    }
                }
            }

            .btn {
                @include button
            }

        }
    }

    h1,
    h3 {
        color: #fff;
    }

    h1 {
        font-size: 40px;
        padding-bottom: 10px;
    }

    .stickers {
        position: absolute;
        right: 15px;
        top: 110px;

        i {
            color: #32465a;
        }

        .green {
            color: $primary;
            font-weight: bolder;
        }

        div {
            text-align: center;
            padding: 10px 5px;
            background-color: #fff;
            margin-bottom: 10px;
            border-radius: 15px;
        }

        span {
            display: block;

            &.txt-sticker {
                color: #32465a;
                font-size: $small-font;
                padding-top: 5px;
            }
        }
    }
}
</style>