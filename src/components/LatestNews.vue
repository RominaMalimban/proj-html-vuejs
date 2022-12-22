<script>
export default {
    name: "LatestNews",
    data() {
        return {
            news: [
                {
                    img: "img/blog-choosecar-700x441.jpg",
                    title: "What Car to Start With?",
                    date: "February 7th 2019 |",
                    comments: "0 Comments",
                    text: "Lorem ipsum dolor sit amet, consectetur adipiscing"
                },
                {
                    img: "img/blogpost-10and2-700x441.jpg",
                    title: "Avada Driving Schhol Expanding",
                    date: "February 7th 2019 |",
                    comments: "0 Comments",
                    text: "Lorem ipsum dolor sit amet, consectetur adipiscing"
                }
            ]
        }
    }
}
</script>

<template>
    <section>

        <div class="container">
            <h2>Latest News</h2>

            <div class="cards">
                <div class="card" v-for="(card, index) in news" :key="index">
                    <img :src="card.img" alt="">
                    <h3>{{ card.title }}</h3>
                    <span>{{ card.date }}</span>
                    <span class="green-color">{{ card.comments }}</span>
                    <p>{{ card.text }}</p>
                </div>

            </div>
            <a href="#">MORE FROM THE BLOG</a>
        </div>
        <div class="angle">
            <img src="../../public/img/latestnews-bottom-800x70.png" alt="">
        </div>
    </section>

</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

section {
    background-image: url(/img/latestnews-background.jpg);
    background-size: cover;
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 860px;
    position: relative;

    .container {
        padding: 70px 0 10px;
        text-align: center;
        background-color: #fff;
        border-top: 5px solid #7195a9;
        border-top-left-radius: 10px;
        border-top-right-radius: 10px;
        position: absolute;
        top: -30px;

        h2 {
            color: $gray-title;
            margin-bottom: 60px;
        }

        .cards {
            @include flex (both);
            padding: 0 30px;

            .card {
                width: calc(100% / 2 - 40px);
                margin-inline: 20px;
                // debug
                // border: 1px solid black;

                h3 {
                    padding: 20px 0 10px;
                    color: $primary;
                }

                span,
                p {
                    color: $gray-text;
                }

                .green-color {
                    color: $primary;
                    padding-left: 5px;
                }

                p {
                    padding: 20px 0 60px;

                }
            }
        }

        a {
            font-size: 14px;
            font-weight: bold;
            color: #fff;
            background-color: $primary;
            padding: 10px 20px;
            border-radius: 30px;
            margin-left: 30px;
        }
    }

    .angle img {
        width: 1200px;
        position: absolute;
        bottom: 75px;
        left: 50%;
        transform: translate(-50%, 0);
    }

}
</style>