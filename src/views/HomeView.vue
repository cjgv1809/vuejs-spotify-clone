<script setup>
import HomeCard from '@/components/HomeCard.vue'

const sections = [
  {
    title: 'Podcasts to make you smarter',
    cards: [
      {
        image: 'https://picsum.photos/id/30/300/300',
        title: 'Title is here',
        subTitle: 'Subtitle is here'
      },
      {
        image: 'https://picsum.photos/id/45/300/300',
        title: 'Title is here',
        subTitle: 'Subtitle is here'
      },
      {
        class: 'md:block hidden',
        image: 'https://picsum.photos/id/65/300/300',
        title: 'Title is here',
        subTitle: 'Subtitle is here'
      },
      {
        class: 'lg:block hidden',
        image: 'https://picsum.photos/id/67/300/300',
        title: 'Title is here',
        subTitle: 'Subtitle is here'
      },
      {
        class: 'xl:block hidden',
        image: 'https://picsum.photos/id/100/300/300',
        title: 'Title is here',
        subTitle: 'Subtitle is here'
      }
    ]
  },
  {
    title: 'Recommended radio',
    cards: [
      {
        image: 'https://picsum.photos/id/120/300/300',
        title: 'Title is here',
        subTitle: 'Subtitle is here'
      },
      {
        image: 'https://picsum.photos/id/110/300/300',
        title: 'Title is here',
        subTitle: 'Subtitle is here'
      },
      {
        class: 'md:block hidden',
        image: 'https://picsum.photos/id/221/300/300',
        title: 'Title is here',
        subTitle: 'Subtitle is here'
      },
      {
        class: 'lg:block hidden',
        image: 'https://picsum.photos/id/232/300/300',
        title: 'Title is here',
        subTitle: 'Subtitle is here'
      },
      {
        class: 'xl:block hidden',
        image: 'https://picsum.photos/id/187/300/300',
        title: 'Title is here',
        subTitle: 'Subtitle is here'
      }
    ]
  },
  {
    title: 'Recommended songs',
    cards: [
      {
        image: 'https://picsum.photos/id/88/300/300',
        title: 'Title is here',
        subTitle: 'Subtitle is here'
      },
      {
        image: 'https://picsum.photos/id/243/300/300',
        title: 'Title is here',
        subTitle: 'Subtitle is here'
      },
      {
        class: 'md:block hidden',
        image: 'https://picsum.photos/id/123/300/300',
        title: 'Title is here',
        subTitle: 'Subtitle is here'
      },
      {
        class: 'lg:block hidden',
        image: 'https://picsum.photos/id/121/300/300',
        title: 'Title is here',
        subTitle: 'Subtitle is here'
      },
      {
        class: 'xl:block hidden',
        image: 'https://picsum.photos/id/99/300/300',
        title: 'Title is here',
        subTitle: 'Subtitle is here'
      }
    ]
  }
]
</script>

<template>
  <div v-for="(section, sectionIndex) in sections" :key="sectionIndex" class="p-8">
    <button type="button" class="text-white text-2xl font-semibold hover:underline cursor-pointer">
      {{ section.title }}
    </button>

    <div class="py-1.5"></div>

    <div class="flex items-center">
      <HomeCard
        v-for="(card, cardIndex) in section.cards"
        :key="cardIndex"
        :image="card.image"
        :title="card.title"
        :subTitle="card.subTitle"
        :class="card.class"
      />
    </div>
  </div>
</template>
