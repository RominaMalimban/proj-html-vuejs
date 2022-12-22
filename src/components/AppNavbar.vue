<script>

export default {
    name: "AppNavbar",
    data() {
        return {
            activeItem: 0,
            logo: "img/avada-drivers-logo-2x-300x58.png",
            links: [
                {
                    text: "HOME",
                    url: "#",
                },
                {
                    text: "ABOUT",
                    url: "#",
                },
                {
                    text: "PRICES",
                    url: "#",
                },
                {
                    text: "COURSES",
                    url: "#",
                    label: "NEW"
                },
                {
                    text: "HOME",
                    url: "#",
                },
                {
                    text: "LOCATIONS",
                    url: "#",
                },
                {
                    text: "BLOG",
                    url: "#",
                }
            ]
        }
    }
}

</script>

<template>

    <!-- nav bar -->
    <nav>
        <div class="container">

            <!-- logo -->
            <a href="#">
                <img :src="logo" alt="logo">
            </a>

            <!-- links -->
            <div class="dx">
                <ul>
                    <li v-for="(link, index) in links" :key="index">
                        <a :href="link.url" :class="activeItem === index ? 'active' : ''">{{ link.text }}</a>
                        <span v-if="link.label" class="new-label">{{ link.label }}</span>
                    </li>
                </ul>

                <a href="#" class="btn">BOOK NOW</a>
            </div>

        </div>
    </nav>
    <!-- chiusura nav bar -->

</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

nav {
    padding: 30px 0;
    background-color: #666b6684;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;

    .container {
        @include flex(both);

        .dx {
            @include flex(both);

            ul {
                @include flex(both);

                li {
                    padding-left: 30px;

                    a {
                        color: $white;
                        font-size: 14px;
                        font-weight: bold;
                        padding: 5px 0;

                        &.active,
                        &:hover {
                            color: $primary;
                            border-bottom: 2px solid $primary;
                        }
                    }

                    .new-label {
                        color: $white;
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
                @include button;
                padding: 8px 13px;
                margin-left: 30px;
            }
        }
    }
}
</style>