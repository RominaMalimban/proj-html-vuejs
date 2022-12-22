<script>
export default {
    name: "SignUp",
    data() {
        return {
            fields: [
                {
                    type: "text",
                    placeholder: "Your Name*"
                },
                {
                    type: "text",
                    placeholder: "Email*"
                },
                {
                    type: "text",
                    placeholder: "Telephone"
                },
                {
                    type: "text",
                    placeholder: "Location"
                }
            ]
        }
    }
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
                <h3>First Lesson Free!</h3>
                <span>When you make a block booking with us your first lesson is included free.</span>

                <!-- form -->
                <form v-for="field in fields">
                    <input :type="field.type" :placeholder="field.placeholder">
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
        color: $gray-text;
        width: 60%;
        padding-right: 50px;

        h2 {
            color: $gray-title;

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

        h3 {
            margin-bottom: 50px;
            color: $primary;
        }

        span {
            color: $gray-text;
        }

        form {
            display: flex;
            flex-direction: column;
            margin: 30px 0;

            input {
                padding: 10px;
                background-color: #f7f7f7;
                border: 1px solid #dfdfdf;
                border-radius: 5px;
                font-size: $smaller-font;
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