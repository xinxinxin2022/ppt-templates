<template>
  <div class="py-12"><div class="max-w-3xl mx-auto px-4 prose prose-lg text-gray-700">
    <h1 class="text-3xl font-bold mb-6">{{ t('terms.title') }}</h1>
    <p><em>{{ t('terms.lastUpdated') }}</em></p>

    <h2>1. Acceptance of Terms</h2>
    <p>By accessing and using PPTTemplates (the "Site"), you accept and agree to be bound by these Terms of Service (the "Terms"). If you do not agree to these Terms, please do not use the Site. We reserve the right to modify these Terms at any time, and such modifications will be effective immediately upon posting.</p>

    <h2>2. Description of Service</h2>
    <p>PPTTemplates provides free PowerPoint and Google Slides presentation templates for download. Our service includes a collection of professionally designed templates organized by category (Business, Creative, Academic, Technology, Marketing), along with blog content about presentation design and tips.</p>

    <h2>3. License to Use Templates</h2>
    <p>All presentation templates on this Site are provided free of charge for both personal and commercial use. You may download, modify, and use the templates to create your own presentations for any purpose, including commercial projects, client work, academic presentations, and internal business use.</p>
    <p>However, you may NOT: resell or redistribute the templates themselves as your own product, claim ownership of the original template designs, use the templates to create a competing template service, or remove any copyright notices if present.</p>

    <h2>4. Intellectual Property</h2>
    <p>The templates, website design, logo, blog content, and all other materials on this Site are owned by PPTTemplates and are protected by applicable intellectual property laws. While we grant you a license to use the templates as described above, all ownership rights remain with us.</p>

    <h2>5. No Warranty</h2>
    <p>All templates and content on this Site are provided "as is" and "as available" without warranty of any kind, either express or implied. We do not guarantee that the templates will meet your specific requirements, that they will be compatible with all presentation software, or that using our templates will result in successful presentations or any specific outcome.</p>

    <h2>6. Limitation of Liability</h2>
    <p>In no event shall PPTTemplates be liable for any direct, indirect, incidental, special, consequential, or exemplary damages arising from your use of the Site or the templates. This includes but is not limited to damages for loss of profits, data, or other intangible losses, even if we have been advised of the possibility of such damages.</p>

    <h2>7. Third-Party Links</h2>
    <p>Our Site may contain links to third-party websites or services that are not owned or controlled by PPTTemplates. We have no control over and assume no responsibility for the content, privacy policies, or practices of any third-party websites or services. You acknowledge and agree that we shall not be responsible or liable for any damage or loss caused by or in connection with the use of any such content, goods, or services available on or through any such websites.</p>

    <h2>8. Advertisement Disclosure</h2>
    <p>Our Site displays advertisements through Google AdSense. These ads may be targeted based on your browsing history and interests. We earn revenue when visitors view or click on these advertisements. The presence of advertisements does not influence our template recommendations or content.</p>

    <h2>9. Changes to Terms</h2>
    <p>We reserve the right to modify these Terms at any time. Changes will be posted on this page with an updated revision date. Your continued use of the Site after any changes constitutes your acceptance of the updated Terms. If you do not agree to the updated Terms, you must stop using the Site.</p>

    <h2>10. Governing Law</h2>
    <p>These Terms shall be governed by and construed in accordance with applicable laws, without regard to conflict of law principles. Any disputes arising from these Terms or your use of the Site shall be resolved through good faith negotiation.</p>

    <h2>11. Contact</h2>
    <p>If you have any questions about these Terms of Service, please <router-link to="/contact" class="text-blue-600 hover:underline">contact us</router-link> or email us at ben357753@163.com.</p>
  </div></div>
</template>
<script setup lang="ts">
import { useI18n } from 'vue-i18n'
const { t } = useI18n()
</script>
