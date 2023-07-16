<template>
    <div class="process">
    <SubHeading title="Our Working Process" description="Step-by-Step Guide to Achieving Your Business Goals" />
  
      <div class="process-block">
        <div class="process-cards">
          <div class="process-card" v-for="(card, index) in cards" :key="index" :style="{ background: card.isOpen ? '#B9FF66' : '#F3F3F3' }">
            <div class="process-card-top">
              <div class="process-card-text">
                <h3 class="process-card-text__number">{{ card.number }}</h3>
                <span class="process-card-text__title">{{ card.title }}</span>
              </div>
  
              <img @click="toggleCard(index)" :src="card.isOpen ? '/svg/plus-icon.svg' : '/svg/minus-icon.svg'">
            </div>
  
            <div class="process-card-bottom" v-if="card.isOpen">
              <p class="process-card-bottom__description">{{ card.description }}</p>
            </div>

          </div>
        </div>
      </div>
    </div>
</template>
  
<script setup>
  import { ref } from 'vue';
  import SubHeading from '@/components/SubHeading.vue';
  
  const cards = ref([
    {
      number: '01',
      title: 'Consultation',
      description: 'During the initial consultation, we will discuss your business goals and objectives, target audience, and current marketing efforts. This will allow us to understand your needs and tailor our services to best fit your requirements.',
      isOpen: true,
    },
    {
      number: '02',
      title: 'Research and Strategy Development',
      description: 'In the planning phase, we will develop a comprehensive strategy for achieving your business goals. This includes identifying key milestones, creating a timeline, and outlining the resources required for successful execution.',
      isOpen: false,
    },
    {
      number: '03',
      title: 'Implementation',
      description: 'In the planning phase, we will develop a comprehensive strategy for achieving your business goals. This includes identifying key milestones, creating a timeline, and outlining the resources required for successful execution.',
      isOpen: false,
    },
    {
      number: '04',
      title: 'Monitoring and Optimization',
      description: 'In the planning phase, we will develop a comprehensive strategy for achieving your business goals. This includes identifying key milestones, creating a timeline, and outlining the resources required for successful execution.',
      isOpen: false,
    },
    {
      number: '05',
      title: 'Reporting and Communication',
      description: 'In the planning phase, we will develop a comprehensive strategy for achieving your business goals. This includes identifying key milestones, creating a timeline, and outlining the resources required for successful execution.',
      isOpen: false,
    },
    {
      number: '06',
      title: 'Continual Improvement',
      description: 'In the planning phase, we will develop a comprehensive strategy for achieving your business goals. This includes identifying key milestones, creating a timeline, and outlining the resources required for successful execution.',
      isOpen: false,
    },
  ]);
  
  const toggleCard = (index) => {
    cards.value.forEach((card, i) => {
      card.isOpen = i === index ? !card.isOpen : false;
    });
  }
  </script>

<style lang="scss" scoped>
    .process {

        &-block {

        }

        &-cards {
            display: grid;
            row-gap: 30px;
        }

        &-card {

            transition: all 0.5s;
            border-radius: 45px;
            border: 1px solid var(--dark);
            background: var(--lightgray);
            padding: 41px 60px;
            box-shadow: 0px 5px 0px 0px var(--dark);

            &-top {
                display: flex;
                align-items: center;
                justify-content: space-between;
            }

            &-bottom {
                border-top: 0.5px solid #000;
                padding: 25px 0 0 0;
                margin: 25px 0 0 0;

                &__description {
                    font-size: 18px;
                    
                }
            }

            &-text {
                display: flex;
                column-gap: 25px;
                align-items: center;

                &__number {
                    font-size: 60px;
                    font-weight: 500;
                }

                &__title {
                    font-size: 30px;
                    font-weight: 500;
                }
            }
        }
    }

</style>