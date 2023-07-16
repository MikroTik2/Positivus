<template>
    <div class="hero">
        <div class="hero-top">
            <div class="hero-right">
                <h1 class="hero-right-title">Navigating the digital landscape for success</h1>
                <span class="hero-right-description">Our digital marketing agency helps businesses grow and succeed online through a range of services including SEO, PPC, social media marketing, and content creation.</span>
            
                <button class="hero-right-btn">Book a consultation</button>
            </div>
                
            <div class="hero-left">
                <img src="/img/hero.jpg" alt="hero-image">
            </div>
        </div>

        <div class="hero-brand">
            <img v-for="brand in brands" :src="brand.img" :alt="brand.name">
        </div>
    </div>
</template>

<script setup>
    import { ref } from 'vue';

    const brands = ref([
        { img: "/brand/amazon-brand.svg", name: "amazon" },
        { img: "/brand/fribbble-brand.svg", name: "fribbble" },
        { img: "/brand/hubspot-brand.svg", name: "hubspot" },
        { img: "/brand/netflix-brand.svg", name: "netflix" },
        { img: "/brand/notion-brand.svg", name: "notion" },
        { img: "/brand/zoom-brand.svg", name: "zoom" },
    ]);
</script>

<style lang="scss" scoped>
    .hero {
        
        &-top {
            display: grid;
            column-gap: 40px;
            grid-template-columns: repeat(2, 1fr);
        }

        &-right {

            &-title {
                font-size: 60px;
                font-weight: 500;
                margin-bottom: 35px;
            }

            &-description {
                margin-bottom: 35px;
                display: block;
            }

            &-btn {
                border-radius: 14px;
                background: var(--dark);
                color: var(--lightgray);
                font-size: 20px;
                cursor: pointer;
                border: none;
                width: 230px;
                height: 68px;
                transition: all .3s;

                &:hover {
                    background: transparent;
                    color: var(--dark);
                    border: 1px solid var(--dark);
                }
            }
        }

        &-brand {
            margin-top: 20px;
            display: flex;
            justify-content: space-between;
        }
    }
</style>