<template>
  <div class="py-12"><div class="max-w-3xl mx-auto px-4">
    <h1 class="text-3xl font-bold mb-6">{{ t('about.title') }}</h1>
    <div class="prose prose-lg text-gray-700 space-y-4">
      <p>{{ t('about.p1') }}</p>
      <h2 class="text-2xl font-bold mt-8">{{ t('about.missionTitle') }}</h2>
      <p>{{ t('about.missionP') }}</p>
      <h2 class="text-2xl font-bold mt-8">{{ t('about.contactTitle') }}</h2>
      <p>{{ t('about.contactP') }}</p>
    </div>
  </div></div>
</template>
<script setup lang="ts">
import { useI18n } from 'vue-i18n'
const { t } = useI18n()
</script>
