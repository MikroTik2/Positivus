<template>
    <div class="hero-info">
        <div class="hero-info-content">
            <h2 class="hero-info-title">Let’s make things happen</h2>
            <span class="hero-info-description">Contact us today to learn more about how our digital marketing services can help your business grow and succeed online.</span>

            <button class="hero-info-btn">Get your free proposal</button>
        </div>

        <img src="/svg/Illustration.svg" alt="Illustration">
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
    .hero-info {
        border-radius: 45px;
        background: #F3F3F3;
        padding: 0px 60px;
        height: 347px;
        display: flex;
        justify-content: space-between;
        align-items: center;

        &-content {
            max-width: 500px;
        }

        &-title {
            font-size: 30px;
            font-weight: 500;
        }

        &-description {
            font-size: 18px;
            margin-top: 25px;
            margin-bottom: 25px;
            display: block;
        }

        &-btn {
            border-radius: 14px;
            border: none;
            font-size: 20px;
            font-weight: 400;
            background: var(--dark);
            height: 68px;
            width: 288px;
            display: flex;
            justify-content: center;
            align-items: center;
            transition: all 0.3s;
            cursor: pointer;
            color: #fff;

            &:hover {
                background: transparent;
                border: 1px solid #000;
                color: #000;
            }
        }
    }
</style>