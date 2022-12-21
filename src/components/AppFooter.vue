<script>
export default {
    name: "AppFooter",
    data() {
        return {
            logo: "img/avada-drivers-logo-2x-200x39.png",
            imgTopFooter: "img/footer-tab.png",

            // array di oggetti per contatti in top-footer:
            contacts: [
                {
                    icon: 'fa-solid fa-house',
                    text: '12345 North Main Street, New York, NY 555555',
                },
                {
                    icon: 'fa-phone-flip',
                    text: '1.800.555.6789',
                },
                {
                    icon: 'fa-envelope',
                    text: 'info@your-domain.com',
                },
                {
                    icon: 'fa-solid fa-link',
                    text: 'Theme-Fusion.com',
                },
            ],

            // array di oggetti per corsi in sub-footer:
            courses: [
                {
                    icon: 'fa-solid fa-arrow-right',
                    text: 'Pass Plus'
                },
                {
                    icon: 'fa-solid fa-arrow-right',
                    text: 'Intensive Course'
                },
                {
                    icon: 'fa-solid fa-arrow-right',
                    text: 'Automatic'
                },
                {
                    icon: 'fa-solid fa-arrow-right',
                    text: 'Instructor Training'
                },
            ],

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
                <!-- logo -->
                <div class="logo">
                    <img :src="logo" alt="logo">
                    <div>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Similique doloremque commodi, maiores
                        unde illum minus delectus nihil dolore natus quo, reiciendis exercitationem molestias dolores
                        qui obcaecati laboriosam animi, assumenda vitae?
                    </div>
                </div>

                <!-- contatti -->
                <div class="contacts">
                    <h4>CONTACT DETAILS</h4>
                    <ul>
                        <li v-for="(contact, index) in contacts" :key="index">
                            <i class="fa-solid" :class="contact.icon"></i>
                            <span>{{ contact.text }}</span>
                        </li>
                    </ul>
                </div>

                <!-- corsi -->
                <div class="courses">
                    <h4>COURSES</h4>
                    <ul>
                        <li v-for="course in courses">
                            <i :class="course.icon"></i>
                            <span>{{ course.text }}</span>
                        </li>
                    </ul>
                </div>

                <!-- book now -->
                <div class="book">
                    <img :src="imgTopFooter" alt="">
                    <a href="#" class="btn">BOOK NOW</a>
                </div>
            </div>

        </div>
        <!-- chiusura top-footer -->

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
    padding: 60px 0;

    .container {
        @include flex(both);
        color: $light-grey;

        h4 {
            color: #fff;
        }

        ul li {
            padding: 10px 0;
        }

        .logo {
            width: 30%;

            div {
                font-size: $small-font;
                padding-top: 15px;
            }
        }

        .contacts {
            h3 {
                padding-bottom: 10px;

            }

            ul li {
                font-size: $small-font;

                i {
                    color: #b5c4cc;
                    padding-right: 10px;
                }
            }
        }

        .courses {

            h3 {
                padding: 5px 0;
            }

            ul li {
                font-size: 13px;
                color: $primary;

                i {
                    font-size: $smaller-font;
                    border: 3px solid $primary;
                    padding: 2px;
                    border-radius: 50%;
                    margin-right: 10px;
                }
            }
        }

        .book {
            width: 25%;
            text-align: center;

            .btn {
                color: #fff;
                background-color: $primary;
                padding: 10px 20px;
                border-radius: 30px;
                display: inline-block;
                text-align: center;
                margin-top: 15px;
                width: auto;
            }

        }
    }
}

.sub-footer {
    background-color: #1c1d1e;

    .container {
        padding: 60px 0;
        font-size: $smaller-font;
        color: $light-grey;
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
