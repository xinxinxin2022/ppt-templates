<template>
  <div class="py-12"><div class="max-w-3xl mx-auto px-4">
    <h1 class="text-3xl font-bold mb-6">{{ t('about.title') }}</h1>
    <div class="prose prose-lg text-gray-700 space-y-4">
      <p>{{ t('about.p1') }}</p>
      <p>Founded in 2026, PPTTemplates was created to solve a common problem: finding high-quality, professional presentation templates that are truly free and easy to use. We noticed that many "free" template sites require sign-ups, have hidden paywalls, or offer low-quality designs that don't work well with modern presentation software.</p>
      <p>Our collection of 99 templates spans five carefully curated categories: Business presentations for corporate meetings and investor pitches, Creative designs for agencies and creative professionals, Academic templates for research presentations and thesis defenses, Technology templates for startup pitches and product launches, and Marketing templates for campaign reports and strategy decks.</p>

      <h2 class="text-2xl font-bold mt-8">{{ t('about.missionTitle') }}</h2>
      <p>{{ t('about.missionP') }}</p>
      <p>We believe that great presentation design should not be limited by budget. Whether you're a student preparing for a thesis defense, a startup founder pitching to investors, a marketing professional presenting campaign results, or a teacher creating educational materials, you deserve access to professional-quality templates. Every template on our site is free to download, free to customize, and free to use for both personal and commercial purposes.</p>

      <h2 class="text-2xl font-bold mt-8">What Makes Us Different</h2>
      <p>Unlike many template sites, we focus on quality over quantity. Each of our 99 templates is carefully selected for professional design, compatibility with both PowerPoint and Google Slides, ATS-friendly formatting, and ease of customization. We don't clutter our site with ads that interrupt your workflow, and we never require you to create an account to download a template.</p>
      <p>All templates are provided in standard .pptx format, ensuring compatibility with Microsoft PowerPoint, Google Slides, Apple Keynote, LibreOffice Impress, and other major presentation software. Simply download, open in your preferred application, and start customizing.</p>

      <h2 class="text-2xl font-bold mt-8">Our Blog</h2>
      <p>Beyond templates, we provide valuable content through our blog. Our articles cover presentation design tips, software comparisons (PowerPoint vs Google Slides), public speaking advice, data visualization best practices, and industry-specific presentation strategies. We publish new content regularly to help you improve not just how your presentations look, but how effectively they communicate your message.</p>

      <h2 class="text-2xl font-bold mt-8">{{ t('about.contactTitle') }}</h2>
      <p>{{ t('about.contactP') }}</p>
      <p>We read every message and typically respond within 24 hours. Whether you have a question about a specific template, want to request a new design, need help with customization, or just want to say hello, we'd love to hear from you. You can also reach us directly at ben357753@163.com.</p>
    </div>
  </div></div>
</template>
<script setup lang="ts">
import { useI18n } from 'vue-i18n'
const { t } = useI18n()
</script>
