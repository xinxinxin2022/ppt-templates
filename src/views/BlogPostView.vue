<template>
  <div class="py-12" v-if="post">
    <div class="max-w-3xl mx-auto px-4">
      <router-link to="/blog" class="text-blue-600 hover:underline mb-4 inline-block">{{ t('blogPost.back') }}</router-link>
      <div class="text-sm text-gray-500 mb-2">{{ post.date }} · {{ post.category }}</div>
      <h1 class="text-4xl font-bold mb-6">{{ post.title }}</h1>
      <div class="prose prose-lg text-gray-700" v-html="post.content"></div>
    </div>
  </div>
</template>
<script setup lang="ts">
import { computed } from 'vue'
import { useRoute } from 'vue-router'
import { useI18n } from 'vue-i18n'
const { t } = useI18n()
const route = useRoute()
const slug = computed(() => route.params.slug as string)
const allPosts: Record<string, any> = {
  'presentation-design-tips': { date: 'Aug 11, 2026', category: 'Design', title: '10 Presentation Design Tips That Actually Work', content: '<h2>1. Less Is More</h2><p>Every slide should convey one key idea. Remove anything that doesn\'t directly support your message. Audiences can\'t read and listen at the same time.</p><h2>2. Use High-Quality Images</h2><p>Replace bullet points with relevant, high-resolution images. Visual information is processed 60,000 times faster than text.</p><h2>3. Consistent Typography</h2><p>Stick to 2 fonts maximum: one for headings, one for body text. Consistency builds professionalism.</p><h2>4. Strategic Color Use</h2><p>Use your brand colors consistently. Use color to highlight key data points, not to decorate.</p><h2>5. Data Visualization</h2><p>Turn numbers into charts. Use bar charts for comparisons, line charts for trends, and pie charts for proportions.</p><h2>6. White Space</h2><p>Don\'t fear empty space. White space improves readability and draws attention to what matters.</p><h2>7. One Idea Per Slide</h2><p>If a slide needs more than 30 seconds to explain, split it. Each slide should support one point.</p><h2>8. Strong Opening</h2><p>Start with a hook: a surprising statistic, a compelling question, or a brief story. Never start with "Today I\'ll talk about..."</p><h2>9. Clear Call to Action</h2><p>End with a clear next step. What should your audience do after this presentation?</p><h2>10. Practice Transitions</h2><p>Smooth transitions between slides show professionalism. Use consistent layouts and visual cues to guide the audience.</p>' },
  'ppt-vs-google-slides': { date: 'Aug 9, 2026', category: 'Tools', title: 'PowerPoint vs Google Slides: Which Is Better in 2026?', content: '<h2>Feature Comparison</h2><p>Both tools have evolved significantly. Here\'s how they compare in 2026.</p><h2>PowerPoint Strengths</h2><p>Advanced animations, 3D models, AI-powered Designer, offline access, extensive template library. Best for complex, polished presentations.</p><h2>Google Slides Strengths</h2><p>Real-time collaboration, cloud-native, free, works on any device, easy sharing. Best for team projects and quick presentations.</p><h2>When to Use PowerPoint</h2><p>Client presentations, conference talks, complex data visualization, offline scenarios, when you need advanced design features.</p><h2>When to Use Google Slides</h2><p>Team collaboration, quick internal updates, remote presentations, when accessibility matters, when budget is a concern.</p><h2>The Verdict</h2><p>Use both. Create in PowerPoint for maximum design control, then upload to Google Slides for collaboration and sharing. Our templates work in both tools.</p>' },
  'how-to-start-presentation': { date: 'Aug 7, 2026', category: 'Tips', title: 'How to Start a Presentation That Captivates Your Audience', content: '<h2>The First 30 Seconds Matter Most</h2><p>Your opening determines whether your audience leans in or zones out. Here are proven techniques.</p><h2>Technique 1: The Surprising Statistic</h2><p>"95% of presentations fail to achieve their goal." Start with a number that shocks your audience into paying attention.</p><h2>Technique 2: The Story</h2><p>"Three years ago, I stood in front of 500 investors with shaking hands..." Stories create emotional connection.</p><h2>Technique 3: The Question</h2><p>"How many of you have ever felt your presentation was ignored?" Questions make the audience active participants.</p><h2>Technique 4: The Bold Statement</h2><p>"Everything you know about presentations is wrong." Challenge assumptions to create curiosity.</p><h2>What to Avoid</h2><p>Never start with "Today I\'ll talk about..." or "Can everyone hear me?" or reading your title slide verbatim.</p>' },
}
const post = computed(() => { const p = allPosts[slug.value]; if (!p) return null; return { ...p, slug: slug.value } })
</script>
