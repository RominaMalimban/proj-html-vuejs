<script>
export default {
    name: "Newsletter",
}
</script>

<template>

    <section>
        <div class="container">
            <h3>Sign up to our Newsletter</h3>
            <form>
                <input type="text">
                <button type="submit">SUBSCRIBE</button>
                <span>(We do not share your data with anybody, and only use it for its intended purpose)</span>
            </form>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

section {
    background-image: url(/img/newsletter_background.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center top;
    padding: 70px 0;
    text-align: center;

    h3 {
        color: $gray-title;
        margin-bottom: 50px;
    }

    form {
        @include flex(col-center);

        input,
        button {
            width: 40%;
            padding: 10px;
        }

        button {
            @include button;
            border: 1px solid $primary;
            margin: 25px 0;
        }

        span {
            font-size: $small-font;
        }
    }
}
</style>