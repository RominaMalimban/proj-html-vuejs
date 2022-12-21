<script>
export default {
    name: "AppFooter",
    data() {
        return {
            logo: "img/avada-drivers-logo-2x-200x39.png",
            // array di oggetti per social in sub-footer:
            socials: [
                {
                    name: 'Facebook',
                    icon: 'fa-facebook-f'
                },
                {
                    name: 'Twitter',
                    icon: 'fa-twitter'
                },
                {
                    name: 'YouTube',
                    icon: 'fa-youtube'
                },
                {
                    name: 'Instagram',
                    icon: 'fa-instagram'
                }
            ]
        }
    }
}
</script>

<template>

    <footer>
        <!-- top-footer -->
        <div class="top-footer">

            <div class="container">
                <div>
                    <img :src="logo" alt="logo">
                    <div>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Similique doloremque commodi, maiores
                        unde illum minus delectus nihil dolore natus quo, reiciendis exercitationem molestias dolores
                        qui obcaecati laboriosam animi, assumenda vitae?
                    </div>
                </div>
                <div></div>
                <div></div>
                <div></div>
            </div>

        </div>

        <!-- sub-footer -->
        <div class="sub-footer">
            <div class="container">
                <div>
                    &copy; Copyright 2 012 - 2020 | Avada Theme by <span>ThemeFusion</span> | All Rights Reserved |
                    Powered
                    by <span>Wordpress</span>
                </div>

                <div class="socials">
                    <ul>
                        <li v-for="social in socials" :key="social.name">
                            <a href="#"><i class="fa-brands" :class="social.icon"></i></a>
                        </li>
                    </ul>
                </div>
            </div>

        </div>
    </footer>

</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

.top-footer {
    background-image: url(../../public/img/footer-background-color.jpg);
    padding: 30px 0;

    .container {
        @include flex(both)
    }
}

.sub-footer {
    background-color: #1c1d1e;

    .container {
        padding: 60px 0;
        font-size: $small-font;
        color: #676360;
        @include flex (both);

        span {
            color: $primary;
        }

        .socials {
            ul {
                display: flex;

                a {
                    color: #fff;
                    padding-left: 15px;
                }
            }


        }


    }
}
</style>
