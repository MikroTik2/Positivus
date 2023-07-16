<template>
    <div class="studies">
        <SubHeading title="Case Studies" description="Explore Real-Life Examples of Our Proven Digital Marketing Success through Our Case Studies"/>

        <div class="studies-hero">
            <div class="studies-content">
                <div class="studies-text" :style="{ borderLeft: list.border, borderRight: list.border }" v-for="list in lists">
                    <span :style="{ padding: list.padding }" class="studies-description"> {{ list.description }} </span>
            
                    <router-link :style="{ padding: list.paddingLink }" class="studies-link" to="/">Learn more <img src="/svg/arrow-default.svg"></router-link>
                </div>
            </div>
        </div>
    </div>
</template> 

<script setup>
    import { ref } from 'vue';
    import SubHeading from '@/components/SubHeading.vue';

    const lists = ref([
        { description: "For a local restaurant, we implemented a targeted PPC campaign that resulted in a 50% increase in website traffic and a 25% increase in sales." },
        { description: "For a B2B software company, we developed an SEO strategy that resulted in a first page ranking for key keywords and a 200% increase in organic traffic.", paddingLink: "0 25px", padding: "0 25px", border: "1px solid #fff" },
        { description: "For a national retail chain, we created a social media marketing campaign that increased followers by 25% and generated a 20% increase in online sales." },
    ]);
</script>

<style lang="scss" scoped>
    .studies {

        &-hero {
            border-radius: 45px;
            padding: 70px 60px;
            background: var(--dark);
        }

        &-content {
            display: grid;
            gap: 65px;
            grid-template-columns: repeat(3, 1fr);
        }

        &-description {
            color: #fff;
            font-size: 18px;
            display: block;
        }

        &-text {
            display: grid;
            align-items: center;
            row-gap: 20px;
            padding: 0 0 10px 0;
        }

        &-link {
            color: var(--green);
            display: flex;
            align-items: center;
            gap: 15px;
        }
    }
</style>