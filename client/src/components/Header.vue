<template>
    <div class="header">
        <div class="header-top">

            <div class="header-top-logo">
                <router-link to="/"> <img src="/svg/positivus-logo.svg" alt="positivus-logo"> </router-link>
            </div>

            <div class="header-top-right">
                <div class="header-top-right-elements">
                    <router-link class="header-top-right__link" :to="element.path" v-for="(element, i) of menu" :key="i"> {{ element.name }} </router-link>
                    <button class="header-top-right__btn">Request a quote</button>
                </div>
                
            </div>
        </div>
    </div>
</template>

<script setup>
    import { ref } from 'vue';

    const menu = ref([
        { path: "/about", name: "About us" },
        { path: "/services", name: "Services" },
        { path: "/cases", name: "Use Cases" },
        { path: "/pricing", name: "Pricing" },
        { path: "/blog", name: "Blog" }
    ])
</script>

<style lang="scss" scoped>
    .header {

        &-top {

            margin-top: 60px;
            margin-bottom: 70px;
            display: flex;
            align-items: center;
            justify-content: space-between;


            &-right {

                display: flex;

                &__btn {
                    border-radius: 14px;
                    background: transparent;
                    font-size: 20px;
                    cursor: pointer;
                    width: 230px;
                    height: 68px;
                    transition: all .3s;
                    border: 1px solid var(--dark);

                    &:hover {
                        background: var(--black);
                        color: var(--lightgray);
                    }
                }

                &-elements {
                    display: flex;
                    align-items: center;
                    column-gap: 40px;
                }

            }
        }
    }
</style>