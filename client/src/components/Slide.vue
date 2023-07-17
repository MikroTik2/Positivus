<template>
    <Carousel :items-to-show="2.5" :wrap-around="true" ref="2.5" v-model="currentSlide">
      <Slide v-for="slide in slides" :key="slide">
        <div class="carousel__item">{{ slide.text }}</div>
      </Slide>
    </Carousel>
  
    <div class="carousel-arrow">
        <img @click="prev" src="/svg/arrow-left.svg">
        <img @click="next" src="/svg/arrow-right.svg">
    </div>
  </template>
  
  

<script setup>
    import { ref } from 'vue';
    import { Carousel, Slide } from 'vue3-carousel';
    import 'vue3-carousel/dist/carousel.css';

    const currentSlide = ref(0);

    const next = () => {
        if (currentSlide.value < slides.value.length - 1) {
            currentSlide.value++;
        }
    };

    const prev = () => {
        if (currentSlide.value > 0) {
            currentSlide.value--;
        }
    };

    const slides = ref([
        { text: '"We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."' },
        { text: '"We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."' },
        { text: '"We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."' },
        { text: '"We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."' },
        { text: '"We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."' },
        { text: '"We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."' },
        { text: '"We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."' },
        { text: '"We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."' },
        { text: '"We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."' },
        { text: '"We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."' }
    ]);

</script>

<style lang="scss" scoped>
    .carousel__item {
        
        color: #fff;
        font-size: 16px;
        border-radius: 45px;
        margin: 0 10px;
        padding: 38px 42px;
        border: 0.5px solid var(--green);
    }
    .carousel-arrow {
        display: flex;
        justify-content: center;
        align-items: center;
        margin-top: 30px;
        gap: 80px;
    }
</style>