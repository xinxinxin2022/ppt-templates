<template>
  <div class="py-12"><div class="max-w-3xl mx-auto px-4 prose prose-lg text-gray-700">
    <h1 class="text-3xl font-bold mb-6">{{ t('privacy.title') }}</h1>
    <p><em>{{ t('privacy.lastUpdated') }}</em></p>

    <h2>1. Information We Collect</h2>
    <p>PPTTemplates is a static website that does not require user accounts, registration, or login to access our templates. We do not collect personal information such as names, email addresses, or phone numbers when you download templates from our site.</p>
    <p>When you visit our website, we automatically collect certain technical information through Google Analytics, including: your IP address (anonymized), browser type and version, operating system, referring URL, pages visited, time spent on each page, and date/time of your visit. This data is used solely to understand how visitors use our site and to improve our content and user experience.</p>

    <h2>2. Cookies and Tracking Technologies</h2>
    <p>We use Google AdSense to display advertisements on our site. Google AdSense uses cookies to serve ads based on your prior visits to our website or other websites on the Internet. These cookies enable Google and its partners to serve ads to you based on your visit to our site and/or other sites on the Internet.</p>
    <p>You may opt out of personalized advertising by visiting Google's Ads Settings at https://www.google.com/settings/ads. You can also opt out of a third-party vendor's use of cookies for personalized advertising by visiting https://www.aboutads.info/choices/.</p>
    <p>Our site does not use Flash cookies or other non-standard tracking technologies. All cookies used are standard HTTP cookies that can be managed through your browser settings.</p>

    <h2>3. How We Use Your Information</h2>
    <p>The analytics data we collect is used for the following purposes: to understand site usage patterns and popular content, to improve our website design and user experience, to identify and fix technical issues, to measure the effectiveness of our content, and to comply with legal obligations.</p>
    <p>We do not use this data to identify individual users or to build personal profiles. We do not sell, trade, rent, or otherwise share your personal information with third parties for their marketing purposes.</p>

    <h2>4. Third-Party Services</h2>
    <p>Our website uses the following third-party services that may collect information: Google Analytics (for website traffic analysis), Google AdSense (for displaying advertisements), and GitHub Pages (for website hosting). Each of these services has its own privacy policy governing how they use your information.</p>
    <p>When you download templates, the files are served from GitHub Releases. GitHub's privacy policy applies to this interaction. We recommend reviewing GitHub's privacy policy at https://docs.github.com/en/site-policy/privacy-policies/github-privacy-statement.</p>

    <h2>5. Data Security</h2>
    <p>We implement reasonable security measures to protect the information we collect. Our website is served over HTTPS, which encrypts data transmitted between your browser and our server. However, no method of transmission over the Internet or method of electronic storage is 100% secure, and we cannot guarantee absolute security.</p>

    <h2>6. Children's Privacy</h2>
    <p>Our website is not directed to children under the age of 13. We do not knowingly collect personal information from children under 13. If you are a parent or guardian and believe that your child has provided us with personal information, please contact us and we will delete such information from our records.</p>

    <h2>7. Your Rights</h2>
    <p>Depending on your location, you may have certain rights regarding your personal information, including the right to access, correct, or delete your data. If you wish to exercise any of these rights, please contact us using the information provided below.</p>
    <p>California residents have additional rights under the California Consumer Privacy Act (CCPA), including the right to know what personal information is collected, the right to delete personal information, and the right to opt-out of the sale of personal information. We do not sell personal information.</p>

    <h2>8. Changes to This Policy</h2>
    <p>We may update this Privacy Policy from time to time to reflect changes in our practices or for other operational, legal, or regulatory reasons. We will post the updated policy on this page with a new revision date. We encourage you to review this policy periodically.</p>

    <h2>9. Contact Us</h2>
    <p>If you have questions or concerns about this Privacy Policy, please contact us at <router-link to="/contact" class="text-blue-600 hover:underline">our contact page</router-link> or email us directly at ben357753@163.com.</p>
  </div></div>
</template>
<script setup lang="ts">
import { useI18n } from 'vue-i18n'
const { t } = useI18n()
</script>
