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

                        <!-- condizione 1: 95% mi mostra l'icona corrispondente -->
                        <i class="fa-solid fa-circle-notch" v-if="rate.percentage === '95%'"></i>

                        <!-- condizione 2 e 3: 100% e 0% mi mostra le icone corrispondenti -->
                        <!-- condizione 4: se 0% aggiungere classe 'different' -->
                        <i class="fa-regular fa-circle" v-if="rate.percentage === '100%' || rate.percentage === '0%'"
                            :class="rate.percentage === '0%' ? 'different' : ''">
                        </i>

                        <!-- condizione per aggiunta pallino verde -->
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

    .cards {
        position: relative;
        top: -130px;
        @include flex(flex);
        margin: -8px;

        .card {
            width: calc(100% / 3 - 16px);
            @include flex (col-center);
            margin: 0 8px;
            background-color: $white;
            border: 1px solid $border-card;
            border-top: 7px solid $primary;
            border-radius: 10px;
            box-shadow: 0px 20px 10px 0px #ebebeb;
            padding: 40px 0;

            .circle {
                position: relative;

                i {
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
                    color: $navy;
                }

                .zero {
                    background-color: $primary;
                    width: 14px;
                    height: 14px;
                    color: $primary;
                    border-radius: 50%;
                    position: absolute;
                    top: 0;
                    left: 50%;
                    transform: translate(-50%, 0);
                }
            }

            .rate {
                display: block;
                padding: 30px 0 60px;
                color: $navy;
            }
        }
    }

}
</style>