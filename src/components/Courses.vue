<script>

import SingleCourse from './SingleCourse.vue';
export default {
    name: "Courses",
    components: {
        SingleCourse
    },

}
</script>

<template>
    <section>
        <div class="container">
            <!-- card grande 'courses' -->
            <div class="courses">
                <h2>Courses</h2>
                <p>
                    Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ratione magni at maiores optio recusandae.
                    Inventore illum harum illo.
                </p>
                <a href="#">COURSE INFORMATION</a>
                <div class="new">
                    <img src="/img/new-corner.jpg" alt="">
                </div>
            </div>
            <!-- chiusura card grande 'courses' -->

            <SingleCourse />
        </div>
    </section>

    <!-- svg triangolo rovesciato -->
    <svg class="fusion-big-triangle-candy" xmlns="http://www.w3.org/2000/svg" version="1.1" width="100%" height="100"
        viewBox="0 0 100 100" preserveAspectRatio="none" style="fill:#e4eaed;padding:0;">
        <path d="M-1 -1 L50 99 L101 -1 Z"></path>
    </svg>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

section {
    background-image: url(/img/promise-background.jpg);
    background-position: cover;
    background-position: 0% 68%;

    .container {
        @include flex (flex);
    }

    // regole div courses
    .courses {
        @include flex(col-center);
        justify-content: center;
        text-align: center;
        background-color: $white;
        border-radius: 10px;
        box-shadow: 0px 20px 10px 0px #bfbebe;
        width: 40%;
        padding: 80px 50px;
        margin-bottom: 110px;
        position: relative;
        top: -35px;

        .new {
            position: absolute;
            top: 0;
            left: 0;
            width: 15%;

            img {
                border-top-left-radius: 10px;
            }
        }

        h2 {
            color: $gray-title;
        }

        p {
            padding: 40px 0;
            line-height: 30px;
            color: $navy;
        }

        a {
            @include button;
            padding: 10px;
            width: 60%;
        }
    }
}

.triangle {
    width: 100%;
}
</style>