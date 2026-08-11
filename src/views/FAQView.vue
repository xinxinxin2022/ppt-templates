<template>
  <div class="py-12">
    <div class="max-w-3xl mx-auto px-4">
      <h1 class="text-3xl font-bold mb-8">{{ t('faq.title') }}</h1>
      <div class="space-y-4">
        <div v-for="(item, i) in faqs" :key="i" class="bg-white rounded-lg border p-6">
          <h3 class="font-semibold text-lg mb-2">{{ item.q }}</h3>
          <p class="text-gray-600">{{ item.a }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import { useI18n } from 'vue-i18n'
const { t } = useI18n()
const faqs = [
  { q: 'Are these presentation templates really free?', a: 'Yes, all templates are completely free to download and use for personal and commercial purposes.' },
  { q: 'What format are the templates?', a: 'All templates are in PowerPoint (.pptx) format, compatible with Microsoft PowerPoint, Google Slides, Keynote, and LibreOffice.' },
  { q: 'Can I use these for Google Slides?', a: 'Yes! Simply upload the .pptx file to Google Drive and open with Google Slides. All formatting is preserved.' },
  { q: 'Can I modify the templates?', a: 'Absolutely. Change colors, fonts, layouts, and content to match your brand and needs.' },
  { q: 'Are the templates ATS-friendly?', a: 'These are presentation templates, not resumes. But they use clean formatting that renders correctly across all presentation software.' },
  { q: 'How many slides per template?', a: 'Templates range from 15 to 50+ slides, covering various presentation needs from short pitches to detailed reports.' },
  { q: 'Can I use these for commercial purposes?', a: 'Yes. All templates are free for both personal and commercial use. You cannot resell the templates themselves.' },
  { q: 'Do I need PowerPoint to use these?', a: 'No. Templates work in Google Slides (free), Keynote (Mac), LibreOffice (free), and any presentation software that supports .pptx.' },
  { q: 'How do I download a template?', a: 'Click the "Download Free" button on any template page. The file will download directly to your computer.' },
  { q: 'Are new templates added regularly?', a: 'Yes, we regularly add new templates across all categories. Check back often for new designs.' },
  { q: 'Can I request a specific template style?', a: 'Yes! Use our Contact page to request specific styles or categories you\'d like to see.' },
  { q: 'What\'s the best template for investor pitches?', a: 'Check our Business category for clean, data-focused templates perfect for investor presentations.' },
  { q: 'Are there templates for academic presentations?', a: 'Yes, our Academic category has templates designed for research presentations, thesis defenses, and lectures.' },
  { q: 'How do I change the color scheme?', a: 'In PowerPoint: Design > Variants > Colors. In Google Slides: Slide > Edit Theme. Change the master colors and all slides update.' },
  { q: 'Can I combine slides from different templates?', a: 'Absolutely. Copy slides between templates to create a custom presentation that meets your exact needs.' },
  { q: 'Do templates include speaker notes?', a: 'Some templates include speaker notes. You can always add your own notes in the notes section of each slide.' },
  { q: 'What resolution are the templates?', a: 'All templates use standard 16:9 widescreen format at 1920x1080 resolution, perfect for modern displays and projectors.' },
  { q: 'Can I print these templates?', a: 'Yes. You can print slides as handouts, notes pages, or full-size slides. PowerPoint and Google Slides both support printing.' },
  { q: 'Are there animation effects included?', a: 'Some templates include subtle transitions and animations. You can modify or remove these as needed.' },
  { q: 'How do I add my logo to all slides?', a: 'In PowerPoint: View > Slide Master > add logo. In Google Slides: Slide > Edit Theme > add logo. It appears on all slides automatically.' },
]
</script>
