<script>
export default {
    name: "Testimonials"
}
</script>

<template>

    <section>
        <div class="container">
            <h2>Testimonials</h2>
            <span>Here&apos;s what our happy drivers had to say about our services:</span>
            <div>
                <img src="/img/testimonial-sophia.png" alt="">
            </div>
            <blockquote>
                <em>Avada Driving School really helped build my confidence behind the wheel and with driving in general,
                    and they got me a first time pass! Highly recommended.</em>
            </blockquote>
            <span id="name">Sophia Jones</span>
            <div>
                <i class="fa-solid fa-circle"></i>
                <i class="fa-regular fa-circle"></i>
                <i class="fa-regular fa-circle"></i>
                <i class="fa-regular fa-circle"></i>
            </div>
        </div>
    </section>

</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as*;

section {
    background-image: url(/img/testimonial-background.jpg);
    background-size: cover;
    padding: 100px 0;

    .container {
        text-align: center;
        color: $navy;
        padding-bottom: 80px;

        h2 {
            color: $gray-title;
            margin: 80px 0 30px;

            +span {
                font-size: 25px;
            }
        }

        img {
            width: 160px;
            margin: 30px 0;
        }

        #name,
        .fa-solid.fa-circle {
            color: $navy;
        }

        em {
            font-size: 18px;
            line-height: 30px;
        }

        #name {
            display: block;
            margin: 30px 0;
        }

        i {
            font-size: $smaller-font;
            padding-inline: 5px;
        }
    }
}
</style>