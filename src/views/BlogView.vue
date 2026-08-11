<template>
  <div class="py-12">
    <div class="max-w-4xl mx-auto px-4">
      <h1 class="text-3xl font-bold mb-8">{{ t('blog.title') }}</h1>
      <div class="space-y-6">
        <article v-for="post in posts" :key="post.slug" class="bg-white rounded-lg shadow-sm border p-6 hover:shadow-md">
          <div class="text-sm text-gray-500 mb-2">{{ post.date }} · {{ post.category }}</div>
          <h2 class="text-2xl font-bold mb-3"><router-link :to="`/blog/${post.slug}`" class="hover:text-blue-600">{{ post.title }}</router-link></h2>
          <p class="text-gray-600 mb-3">{{ post.excerpt }}</p>
          <router-link :to="`/blog/${post.slug}`" class="text-blue-600 hover:underline font-medium">{{ t('blog.readMore') }}</router-link>
        </article>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import { useI18n } from 'vue-i18n'
const { t } = useI18n()
const posts = [
  { slug: 'presentation-design-tips', title: '10 Presentation Design Tips That Actually Work', date: 'Aug 11, 2026', category: 'Design', excerpt: 'Learn the design principles that make presentations memorable and effective.' },
  { slug: 'ppt-vs-google-slides', title: 'PowerPoint vs Google Slides: Which Is Better in 2026?', date: 'Aug 9, 2026', category: 'Tools', excerpt: 'A comprehensive comparison of the two most popular presentation tools.' },
  { slug: 'how-to-start-presentation', title: 'How to Start a Presentation That Captivates Your Audience', date: 'Aug 7, 2026', category: 'Tips', excerpt: 'The opening of your presentation sets the tone. Here are proven techniques.' },
  { slug: 'data-visualization-ppt', title: 'Best Practices for Data Visualization in Presentations', date: 'Aug 5, 2026', category: 'Design', excerpt: 'Turn complex data into compelling visual stories that your audience understands.' },
  { slug: 'pitch-deck-essentials', title: 'Essential Slides Every Startup Pitch Deck Needs', date: 'Aug 3, 2026', category: 'Business', excerpt: 'The must-have slides that investors expect to see in your pitch deck.' },
  { slug: 'presentation-anxiety', title: 'How to Overcome Presentation Anxiety: A Complete Guide', date: 'Aug 1, 2026', category: 'Tips', excerpt: 'Practical strategies to manage nerves and deliver confident presentations.' },
  { slug: 'color-theory-presentations', title: 'Color Theory for Presentations: A Practical Guide', date: 'Jul 29, 2026', category: 'Design', excerpt: 'How to use color effectively to enhance your message and brand.' },
  { slug: 'remote-presentations', title: 'Tips for Delivering Great Remote Presentations', date: 'Jul 27, 2026', category: 'Tips', excerpt: 'Best practices for virtual presentations that keep your audience engaged.' },
  { slug: 'storytelling-presentations', title: 'The Art of Storytelling in Business Presentations', date: 'Jul 25, 2026', category: 'Business', excerpt: 'How to weave compelling narratives into your professional presentations.' },
  { slug: 'accessibility-presentations', title: 'Making Your Presentations Accessible to Everyone', date: 'Jul 23, 2026', category: 'Tips', excerpt: 'Design inclusive presentations that work for all audience members.' },
]
</script>
