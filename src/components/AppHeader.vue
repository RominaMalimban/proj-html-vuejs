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
                    current: false
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
                        <img :src="logo" alt="">
                    </a>
                    <ul>
                        <li v-for="(link, index) in links" :key="index">
                            <a :href="link.url" :class="{ active: link.current }">{{ link.text }}</a>
                        </li>
                    </ul>

                    <a href="#" class="btn">BOOK NOW</a>
                </div>
            </nav>
            <!-- chiusura nav bar -->

            <div class="container">
                <h1>{{ title }}</h1>
                <h3>We offer the finest driving tuition money can buy</h3>
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

    .container {
        height: 100%;
        @include flex(both);
        color: $light-grey;
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

            ul {
                @include flex(both);

                li {
                    padding-left: 40px;

                    a {
                        color: #fff;

                        &.active {
                            color: $primary;
                            border-bottom: 3px solid $primary;
                        }
                    }
                }
            }

            .btn {
                color: #fff;
                background-color: $primary;
                padding: 10px 20px;
                border-radius: 30px;
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
}
</style>