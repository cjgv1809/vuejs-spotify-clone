<script setup>
import CategorySelect from '@/components/CategorySelect.vue'

const categories = [
  { category: 'Podcasts', image: 'https://picsum.photos/id/40/300/300' },
  { category: 'Audiobooks', image: 'https://picsum.photos/id/45/300/300' },
  { category: 'Made For You', image: 'https://picsum.photos/id/76/300/300' },
  { category: 'New Release', image: 'https://picsum.photos/id/56/300/300' },
  { category: 'New Release', image: 'https://picsum.photos/id/25/300/300' },
  { category: 'Podcasts', image: 'https://picsum.photos/id/103/300/300' },
  { category: 'Audiobooks', image: 'https://picsum.photos/id/244/300/300' },
  { category: 'Made For You', image: 'https://picsum.photos/id/202/300/300' },
  { category: 'New Release', image: 'https://picsum.photos/id/101/300/300' },
  { category: 'New Release', image: 'https://picsum.photos/id/120/300/300' }
]
</script>

<template>
  <div class="p-8">
    <button type="button" class="text-white text-2xl font-semibold hover:underline cursor-pointer">
      Browse all
    </button>

    <div class="py-1.5"></div>

    <div class="grid xl:grid-cols-5 lg:grid-cols-4 md:grid-cols-3 sm:grid-cols-2 gap-6">
      <CategorySelect
        v-for="(item, index) in categories"
        :key="index"
        :category="item.category"
        :image="item.image"
      />
    </div>
  </div>
</template>
