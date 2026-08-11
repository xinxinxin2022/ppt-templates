<template>
  <div class="min-h-screen bg-gray-50 flex flex-col">
    <header class="bg-white shadow-sm border-b sticky top-0 z-50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between items-center h-16">
          <router-link to="/" class="flex items-center gap-2">
            <Presentation class="w-7 h-7 text-blue-600" />
            <span class="text-xl font-bold text-gray-900">{{ t('footer.brand') }}</span>
          </router-link>
          <nav class="hidden md:flex items-center gap-6">
            <router-link to="/templates" class="text-gray-700 hover:text-blue-600 font-medium text-sm">{{ t('nav.templates') }}</router-link>
            <router-link to="/category/business" class="text-gray-700 hover:text-blue-600 font-medium text-sm">{{ t('nav.business') }}</router-link>
            <router-link to="/category/creative" class="text-gray-700 hover:text-blue-600 font-medium text-sm">{{ t('nav.creative') }}</router-link>
            <router-link to="/category/academic" class="text-gray-700 hover:text-blue-600 font-medium text-sm">{{ t('nav.academic') }}</router-link>
            <router-link to="/category/technology" class="text-gray-700 hover:text-blue-600 font-medium text-sm">{{ t('nav.tech') }}</router-link>
            <router-link to="/category/marketing" class="text-gray-700 hover:text-blue-600 font-medium text-sm">{{ t('nav.marketing') }}</router-link>
            <router-link to="/blog" class="text-gray-700 hover:text-blue-600 font-medium text-sm">{{ t('nav.blog') }}</router-link>
            <router-link to="/faq" class="text-gray-700 hover:text-blue-600 font-medium text-sm">{{ t('nav.faq') }}</router-link>
          </nav>
          <div class="flex items-center gap-3 md:hidden">
            <button @click="toggleLang" class="text-sm bg-gray-100 hover:bg-gray-200 text-gray-700 px-3 py-1 rounded-full font-medium">{{ t('lang') }}</button>
            <button @click="mobileMenu = !mobileMenu"><Menu class="w-6 h-6" /></button>
          </div>
        </div>
      </div>
      <div v-if="mobileMenu" class="md:hidden border-t bg-white">
        <div class="px-4 py-3 space-y-2">
          <router-link to="/templates" class="block py-2 text-gray-700" @click="mobileMenu = false">{{ t('nav.all') }}</router-link>
          <router-link v-for="cat in cats" :key="cat.slug" :to="`/category/${cat.slug}`" class="block py-2 text-gray-700" @click="mobileMenu = false">{{ cat.label }}</router-link>
          <router-link to="/blog" class="block py-2 text-gray-700" @click="mobileMenu = false">{{ t('nav.blog') }}</router-link>
          <router-link to="/faq" class="block py-2 text-gray-700" @click="mobileMenu = false">{{ t('nav.faq') }}</router-link>
        </div>
      </div>
    </header>
    <main class="flex-1"><router-view /></main>
    <footer class="bg-gray-900 text-gray-400 py-12 mt-16">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
          <div>
            <h3 class="text-white font-bold mb-4">{{ t('footer.brand') }}</h3>
            <p class="text-sm">{{ t('footer.tagline') }}</p>
            <p class="text-sm mt-3"><a href="mailto:ben357753@163.com" class="text-gray-400 hover:text-white">ben357753@163.com</a></p>
          </div>
          <div>
            <h4 class="text-white font-semibold mb-3">{{ t('footer.templates') }}</h4>
            <ul class="space-y-2 text-sm">
              <li v-for="cat in cats" :key="cat.slug"><router-link :to="`/category/${cat.slug}`" class="hover:text-white">{{ cat.label }}</router-link></li>
            </ul>
          </div>
          <div>
            <h4 class="text-white font-semibold mb-3">{{ t('footer.resources') }}</h4>
            <ul class="space-y-2 text-sm">
              <li><router-link to="/blog" class="hover:text-white">{{ t('nav.blog') }}</router-link></li>
              <li><router-link to="/faq" class="hover:text-white">{{ t('nav.faq') }}</router-link></li>
              <li><router-link to="/about" class="hover:text-white">{{ t('nav.about') }}</router-link></li>
              <li><router-link to="/contact" class="hover:text-white">{{ t('nav.contact') }}</router-link></li>
            </ul>
          </div>
          <div>
            <h4 class="text-white font-semibold mb-3">{{ t('footer.legal') }}</h4>
            <ul class="space-y-2 text-sm">
              <li><router-link to="/privacy-policy" class="hover:text-white">{{ t('nav.privacy') }}</router-link></li>
              <li><router-link to="/terms-of-service" class="hover:text-white">{{ t('nav.terms') }}</router-link></li>
            </ul>
          </div>
        </div>
        <div class="border-t border-gray-800 mt-8 pt-8 text-sm text-center"><p>{{ t('footer.copyright') }}</p></div>
      </div>
    </footer>
  </div>
</template>
<script setup lang="ts">
import { ref } from 'vue'
import { useI18n } from 'vue-i18n'
import { Presentation, Menu } from 'lucide-vue-next'
const { t, locale } = useI18n()
const mobileMenu = ref(false)
const cats = [
  { slug: 'business', label: t('nav.business') },
  { slug: 'creative', label: t('nav.creative') },
  { slug: 'academic', label: t('nav.academic') },
  { slug: 'technology', label: t('nav.tech') },
  { slug: 'marketing', label: t('nav.marketing') },
]
function toggleLang() { locale.value = locale.value === 'en' ? 'zh' : 'en'; localStorage.setItem('locale', locale.value) }
</script>
