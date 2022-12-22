<script>

export default {
    name: "SingleCourse",
    data() {
        return {
            // array oggetti per cards:
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
    <div class="cards" v-for="(course, index) in courses" :key="index">
        <div class="card">
            <img :src="course.image" :alt="course.name">
            <h4>{{ course.name }}</h4>
            <a href="#">{{ course.description }}</a>
        </div>
    </div>

</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

.cards {
    @include flex (flex);
    text-align: center;
    padding: 50px 15px;
    margin-left: 30px;

    h4 {
        padding: 20px 0;
        color: $text-course;
    }

    a {
        font-size: 12px;
        font-weight: bold;
        color: $text-course;
        border: 3px solid $text-course;
        border-radius: 30px;
        border-radius: 30px;
        padding: 5px 10px;

        &:hover {
            border-color: $primary;
            color: $primary;
        }
    }
}
</style>