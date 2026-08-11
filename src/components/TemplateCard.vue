<template>
  <router-link :to="`/templates/${template.id}`" class="block bg-white rounded-lg shadow-sm border overflow-hidden hover:shadow-md transition-shadow group">
    <div class="aspect-[16/9] bg-gray-100 rounded-t-lg overflow-hidden mb-3">
      <img :src="template.preview" :alt="template.name" class="w-full h-full object-cover" loading="lazy" />
    </div>
    <div class="p-4">
      <h3 class="font-semibold text-gray-900 mb-1">{{ template.name }}</h3>
      <div class="flex items-center gap-2 mb-2">
        <span class="px-2 py-0.5 rounded-full bg-blue-100 text-blue-700 text-xs">{{ template.category }}</span>
        <span class="px-2 py-0.5 rounded-full bg-gray-100 text-gray-600 text-xs">{{ template.style }}</span>
      </div>
      <p class="text-sm text-gray-500">{{ template.slides }} {{ t('detail.slides') }} · {{ template.color }}</p>
    </div>
  </router-link>
</template>
<script setup lang="ts">
import { useI18n } from 'vue-i18n'
const { t } = useI18n()
defineProps<{ template: any }>()
</script>
