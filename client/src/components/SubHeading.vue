<template>
    <div class="heading">
        <h2 class="heading-title">{{ title }}</h2>
        <span class="heading-description"> {{ description }} </span>
    </div>
</template>

<script setup>

    const props = defineProps({
        title: {
            type: String,
            required: false
        },

        description: {
            type: String,
            required: false
        }
    })
</script>

<style lang="scss" scoped>
    .heading {

        display: flex;
        margin-top: 120px;
        margin-bottom: 85px;
        align-items: center;
        column-gap: 40px;

        &-title {
            font-size: 40px;
            padding: 0px 7px;
            border-radius: 7px;
            background: var(--green);
            font-weight: 500;
        }

        &-description {
            max-width: 580px;
            font-size: 18px;
        }
    }
</style>