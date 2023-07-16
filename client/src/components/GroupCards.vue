<template>
    <div class="cards">

        <SubHeading title="Team" description="Meet the skilled and experienced team behind our successful digital marketing strategies"/>

        <div class="cards-elements">
            <div class="cards-element" v-for="(element, i) of cards" :key="i">
                <div class="cards-element-top">
                    <img :src="element.img">

                    <div class="cards-element-top__name">
                        <h3>{{ element.firstname }}</h3>
                        <span>{{ element.lastname }}</span>
                    </div>

                </div>

                <div class="cards-element-bottom">
                    <p class="cards-element-bottom__description">{{ element.description }}</p>
                </div>
            </div>
        </div>

        <div class="cards-buttons">
            <router-link to="/">
                <button class="cards-button">See all team</button>
            </router-link>
        </div>
    </div>
</template>

<script setup>
    import { ref } from 'vue';
    import SubHeading from '@/components/SubHeading.vue';

    const cards = ref([
        { img: "/team/avatar-1.png", firstname: "John Smith", lastname: "CEO and Founder", description: "10+ years of experience in digital marketing. Expertise in SEO, PPC, and content strategy" },
        { img: "/team/avatar-2.png", firstname: "Jane Doe", lastname: "Director of Operations", description: "7+ years of experience in project management and team leadership. Strong organizational and communication skills" },
        { img: "/team/avatar-3.png", firstname: "Michael Brown", lastname: "Senior SEO Specialist", description: "5+ years of experience in SEO and content creation. Proficient in keyword research and on-page optimization" },
        { img: "/team/avatar-4.png", firstname: "Emily Johnson", lastname: "PPC Manager", description: "3+ years of experience in paid search advertising. Skilled in campaign management and performance analysis" },
        { img: "/team/avatar-5.png", firstname: "Brian Williams", lastname: "Social Media Specialist", description: "4+ years of experience in social media marketing. Proficient in creating and scheduling content, analyzing metrics, and building engagement" },
        { img: "/team/avatar-6.png", firstname: "Sarah Kim", lastname: "Content Creator", description: "2+ years of experience in writing and editing Skilled in creating compelling, SEO-optimized content for various industries" },
    ])
</script> 

<style lang="scss" scoped>
    .cards {

        &-elements {
            display: grid;
            gap: 40px;
            margin-bottom: 40px;
            grid-template-columns: repeat(3, 1fr);
        }

        &-element {

            border-radius: 45px;
            padding: 40px 35px;
            border: 1px solid var(--dark);
            background: #FFF;
            box-shadow: 0px 5px 0px 0px var(--dark);
            
            &-top {
                display: flex;
                align-items: end;
                gap: 20px;
            }

            &-bottom {

                &__description {
                    font-size: 18px;
                    border-top: 0.5px solid #000;
                    padding-top: 25px;
                    margin-top: 25px;
                }
            }
        }

        &-buttons {
            display: flex;
            justify-content: flex-end;
        }

        &-button {
            border-radius: 14px;
            border: none;
            color: #fff;
            width: 269px;
            font-size: 20px;
            font-weight: 400;
            height: 68px;
            cursor: pointer;
            transition: all 0.3s;
            background: var(--dark);

            &:hover {
                background: transparent;
                border: 1px solid #000;
                color: #000;
            }
        }
    }
</style>