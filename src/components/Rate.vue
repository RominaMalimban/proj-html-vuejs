<script>
export default {
    name: "Rate",
    data() {
        return {
            rates: [
                {
                    percentage: "95%",
                    type: "PASS RATE"
                },
                {
                    percentage: "100%",
                    type: "REFFERRAL RATE"
                },
                {
                    percentage: "0%",
                    type: "ACCIDENT RATE"
                },
            ]
        }
    }
}
</script>

<template>

    <section>
        <div class="container">
            <div class="cards">
                <div class="card" v-for="(rate, index) in rates" :key="index">
                    <div class="circle">
                        <i class="fa-solid fa-circle-notch" v-if="rate.percentage === '95%'"></i>
                        <i class="fa-regular fa-circle" v-if="rate.percentage === '100%' || rate.percentage === '0%'"
                            :class="rate.percentage === '0%' ? 'different' : ''">
                        </i>
                        <div class="zero" v-if="rate.percentage === '0%'"></div>
                        <span>{{ rate.percentage }}</span>
                    </div>
                    <span class="rate">{{ rate.type }}</span>
                </div>

            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

section {



    .container {


        .cards {
            position: relative;
            top: -80px;
            display: flex;
            margin: -5px;

            .card {
                width: calc(100% / 3 - 10px);
                margin: 0 5px;
                background-color: #fff;
                border: 1px solid #c1c1c1;
                border-top: 7px solid $primary;
                border-radius: 10px;
                box-shadow: 0px 20px 10px 0px #b7bec2;
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;

                .circle {
                    position: relative;

                    i {
                        padding-top: 20px;
                        font-size: 150px;
                        color: $primary;

                        &.different {
                            color: #f5f5f5;
                        }
                    }

                    span {
                        position: absolute;
                        top: 50%;
                        left: 50%;
                        transform: translate(-50%, -50%);
                        font-size: 30px;
                        color: $gray-text;
                    }

                    .zero {
                        background-color: $primary;
                        width: 14px;
                        height: 14px;
                        color: $primary;
                        border-radius: 50%;
                        position: absolute;
                        top: 20px;
                        left: 50%;
                        transform: translate(-50%, 0);
                    }
                }

                .rate {
                    display: block;
                    padding: 30px 0 60px;
                    color: $gray-text;
                }
            }
        }
    }
}
</style>