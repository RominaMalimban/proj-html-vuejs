<script>
export default {
    name: "Instructors",
    data() {
        return {
            instructors: [
                {
                    name: 'Mike Hart',
                    image: 'img/instructor-mikehart-400x254.jpg',
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.'
                },
                {
                    name: 'John Smith',
                    image: 'img/instructor-johnsmith-400x254.jpg',
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.'
                },
                {
                    name: 'Angela Hart',
                    image: 'img/instructor-angelahart-400x254.jpg',
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.'
                }
            ]
        }
    }
}
</script>

<template>
    <section>
        <div class="container">
            <h2>Your Instructors</h2>
            <div class="top">
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus id fugiat mollitia incidunt hic
                    recusandae magni facilis perferendis rerum, quaerat eos officiis? Nulla rem fugiat impedit sit
                    blanditiis qui corrupti.
                </p>
                <a href="#">MORE ABOUT US</a>
            </div>

            <!-- card -->
            <div class="cards">
                <div class="card" v-for="(instructor, index) in instructors" :key="index">
                    <img :src="instructor.image" :alt="instructor.name">
                    <h4>{{ instructor.name }}</h4>
                    <div>
                        <i class="fa-brands fa-facebook-f"></i>
                        <i class="fa-brands fa-twitter"></i>
                        <i class="fa-brands fa-instagram"></i>
                    </div>
                    <p>{{ instructor.description }}</p>
                </div>
            </div>
        </div>
    </section>

</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

.container {
    position: relative;
    height: 600px;

    h2 {
        color: $gray-title;
    }

    .top {
        @include flex (between);
        padding: 55px 0 80px;

        p {
            color: $navy;
        }

        a {
            @include button;
            width: 35%;
            text-align: center;
            padding: 10px 40px;
        }
    }

    // regole cards
    .cards {
        @include flex(flex);
        margin-inline: - 5px;

        .card {
            width: calc(100% / 3 - 10px);
            margin-inline: 5px;
            text-align: center;
            padding: 40px 40px 80px;
            border: 1px solid #c1c1c1;
            border-top: 7px solid $primary;
            border-radius: 10px;
            box-shadow: 0px 20px 10px 0px #b7bec2;
            background-color: $white;

            h4 {
                padding: 30px 0 15px;
                color: $gray-title;
            }

            i,
            p {
                color: $navy;
                line-height: 25px;
            }

            i {
                padding: 10px;
            }

            &:hover img {
                scale: 1.1;
                box-shadow: 0px 20px 10px 0px #b7bec2;
            }
        }


    }

    .cards .card:nth-child(1),
    .cards .card:nth-child(3) {
        height: 450px;
    }
}
</style>