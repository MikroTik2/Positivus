<template>
    <div class="comment">
        <SubHeading title="Testimonials" description="Hear from Our Satisfied Clients: Read Our Testimonials to Learn More about Our Digital Marketing Services"/>

        <div class="comment-content">
            <Slide />
        </div>
    </div>
</template>

<script setup>
    import SubHeading from '@/components/SubHeading.vue';
    import Slide from '@/components/Slide.vue';
</script>

<style lang="scss" scoped>
    .comment {
        
        &-content {
            border-radius: 45px;
            padding: 84px 0px 68px 0px;
            background: var(--dark);
        }
    }
</style>