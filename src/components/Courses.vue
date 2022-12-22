<script>
export default {
    name: "Courses",
    data() {
        return {
            courses: [
                {
                    name: 'Pass Plus',
                    image: 'img/courses-passplus-200x200.jpg',
                    description: 'LEARN MORE'
                },
                {
                    name: 'Intensive Course',
                    image: 'img/course-intensive-200x200.jpg',
                    description: 'LEARN MORE'
                },
                {
                    name: 'Instructors',
                    image: 'img/courses-instructor-200x200.jpg',
                    description: 'LEARN MORE'
                },
            ]
        }
    }
}
</script>

<template>
    <section>
        <div class="container">
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

            <div class="cards" v-for="(course, index) in courses" :key="index">
                <div class="card">
                    <img :src="course.image" :alt="course.name">
                    <h4>{{ course.name }}</h4>
                    <a href="#">{{ course.description }}</a>
                </div>
            </div>
        </div>
    </section>
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
    // debug
    // min-height: 500px;

    .container {
        display: flex;
    }

    .courses {
        background-color: #fff;
        width: 40%;
        padding: 120px 50px;
        text-align: center;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        position: relative;
        top: -20px;
        border-radius: 10px;
        box-shadow: 0px 20px 10px 0px #bfbebe;
        margin-bottom: 100px;

        h2 {
            color: $gray-title;
        }

        p {
            padding: 40px 0;
            line-height: 30px;
            color: $gray-text;
        }

        a {
            @include button;
            padding: 10px;
            width: 60%;
        }

        .new {
            position: absolute;
            top: 0;
            left: 0;
            width: 15%;

            img {
                border-top-left-radius: 10px;
            }
        }
    }

    .cards {
        margin-left: 30px;
        display: flex;
        padding: 50px 15px;
        text-align: center;
        // width: 60%;

        .card {
            // padding: 0 15px;
            // debug
            // border: 1px solid black;

            h4 {
                padding: 20px 0;
                color: #7697ac;
            }

            a {
                font-size: 12px;
                font-weight: bold;
                color: #7697ac;
                border-radius: 30px;
                border: 3px solid #7697ac;
                border-radius: 30px;
                padding: 5px 10px;

            }
        }
    }
}

.triangle {
    width: 100%;
}
</style>