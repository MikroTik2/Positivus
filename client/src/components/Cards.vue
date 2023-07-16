<template>
    <div class="card">
        <SubHeading title="Services" description="At our digital marketing agency, we offer a range of services to help businesses grow and succeed online. These services include:"/>

        <div class="card-elements">
            <div class="card-element" v-for="(element, i) of cards" :key="i" :style="{ background: element.color }">
                <div class="card-element-right">
                    <div class="card-element-text">
                        <h3 class="card-element-title" :style="{ background: element.colorBackground }"> {{ element.titleOne }} </h3>
                        <h3 class="card-element-title" :style="{ background: element.colorBackground }"> {{ element.titleTwo }} </h3>
                    </div>

                    <router-link :style="{ color: element.colorLink }" class="card-element__link" to="/"> <img :src="element.arrow" alt="arrow-icon"> Learn more</router-link>
                </div>
                <div class="card-element-left">
                    <img :src="element.img" :alt="element.titleOne">
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
    import SubHeading from '@/components/SubHeading.vue';
    import { ref } from 'vue';

    const cards = ref([
        { titleOne: "Search engine", titleTwo: "optimization", img: "/img/tokyo-browser-window-with-emoticon-likes-and-stars-around.png", arrow: "/svg/arrow-green.svg", colorBackground: "#B9FF66", color: "#F3F3F3" },
        { titleOne: "Social Media", titleTwo: "Marketing", img: "/img/tokyo-magnifier-web-search-with-elements.png", arrow: "/svg/arrow-green.svg", colorBackground: "#FFF", color: "#B9FF66" },
        { titleOne: "Content", titleTwo: "Creation", img: "/img/tokyo-many-browser-windows-with-different-information.png", arrow: "/svg/arrow.svg", colorLink: "#FFF", colorBackground: "#FFF", color: "#191A23" },
        { titleOne: "Pay-per-click", titleTwo: "advertising", img: "/img/tokyo-selecting-a-value-in-the-browser-window.png", arrow: "/svg/arrow-green.svg", colorBackground: "#B9FF66", color: "#F3F3F3" },
        { titleOne: "Email", titleTwo: "Marketing", img: "/img/tokyo-sending-messages-from-one-place-to-another.png", arrow: "/svg/arrow-green.svg", colorBackground: "#FFF", color: "#B9FF66" },
        { titleOne: "Analytics and ", titleTwo: "Tracking", img: "/img/tokyo-volumetric-analytics-of-different-types-in-web-browsers.png", arrow: "/svg/arrow.svg", colorLink: "#FFF", colorBackground: "#B9FF66", color: "#191A23" },

    ])
</script>

<style lang="scss" scoped>
    .card {
        margin-bottom: 120px;

        &-elements {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 40px;
        }

        &-element {
            display: flex;
            padding: 50px;
            border-radius: 45px;
            border: 1px solid var(--dark, #191A23);
            box-shadow: 0px 5px 0px 0px #191A23;
            justify-content: space-between;
            transform: translateY(0);
            transition: all 0.3s;

            &:hover {
                transform: translateY(-5px);
            }

            &-right {
                display: flex;
                flex-direction: column;
                justify-content: space-between;
            }

            &-title {
                padding: 0 7px;
                border-radius: 7px;
                font-size: 30px;
                font-weight: 500;
            }

            &__link {
                display: flex;
                align-items: center;
                column-gap: 15px;
            }
        }
    }
</style>