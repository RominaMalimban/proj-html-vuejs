<script>
export default {
    name: "SignUp"
}
</script>

<template>

    <section>
        <div class="container">
            <!-- parte sx -->
            <div class="sx">
                <h2>Get Behind The Wheel</h2>
                <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quos accusamus, quasi, natus dolorum
                    tempore
                    atque omnis laborum eveniet dignissimos doloribus ab corrupti officiis quo voluptates. Adipisci modi
                    dicta culpa eum.
                </p>
                <p class="different-size">
                    Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nisi voluptatum quam explicabo similique,
                    facilis est ipsam voluptate sapiente dolore error mollitia nobis iure officia expedita voluptates
                    alias maiores, quisquam atque? sapiente dolore error mollitia nobis iure officia expedita voluptates
                    alias maiores, quisquam atque? sapiente dolore error mollitia nobis iure officia expedita voluptates
                    alias maiores, quisquam atque?
                </p>
            </div>
            <!-- chiusura parte sx -->

            <!-- parte dx -->
            <div class="dx">
                <h2>First Lesson Free!</h2>
                <span>When you make a block booking with us your first lesson is included free.</span>

                <!-- form -->
                <form>
                    <input type="text" placeholder="You Name*">
                    <input type="text" placeholder="Email*">
                    <input type="text" placeholder="Telephone">
                    <input type="text" placeholder="Location">
                </form>

                <a href="#">REQUEST A CALLBACK</a>
            </div>
            <!-- chiusura parte dx -->
        </div>

        <div>

        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

section {
    background-color: #fff;
    padding: 90px 0 230px;

    .container {
        @include flex(both);
        position: relative;

    }

    .sx {
        color: #a7adb5;
        width: 60%;
        padding-right: 50px;

        h2 {
            color: $gray-title;
            font-size: 30px;

            +p {
                margin: 30px 0;
            }
        }

        .different-size {
            font-size: 14px;
        }
    }

    .dx {
        width: 40%;
        margin-left: 50px;
        background-color: #fff;
        text-align: center;
        border: 1px solid #eaeaea;
        border-radius: 10px;
        padding: 50px;
        position: absolute;
        right: 0;
        box-shadow: 0px 20px 10px 0px #ececec;

        h2 {
            margin-bottom: 50px;
            color: $primary;
        }

        span {
            color: #a7adb5;
        }

        form {
            display: flex;
            flex-direction: column;
            margin: 30px 0;

            input {
                padding: 10px;
                margin: 10px 0;
                background-color: #f7f7f7;
                border: 1px solid #a7adb5;
                border-radius: 3px;
            }
        }

        a {
            color: #fff;
            background-color: $primary;
            padding: 10px 20px;
            border-radius: 30px;
        }
    }
}
</style>