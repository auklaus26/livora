<script setup lang="ts">
import { siteEmail, siteLocation, siteName, sitePhone } from '~/composables/useSiteContent'

useHead({
  title: 'Website Terms and Conditions | Livora Care'
})

const sections = [
  {
    title: 'Introduction',
    body:
      'These Terms and Conditions govern the use of the Livora Care website. By accessing or using this website, you acknowledge that you have read, understood and agree to comply with these terms.'
  },
  {
    title: 'Purpose and Use of the Website',
    body:
      'The website provides general information about Livora Care, our disability support services and ways to contact or collaborate with our organisation. Users must use the website lawfully and respectfully.'
  },
  {
    title: 'Accuracy of Information',
    body:
      'We make reasonable efforts to ensure information published on the website is accurate and current at the time of publication, but service environments and requirements may evolve over time.'
  },
  {
    title: 'Intellectual Property',
    body:
      'All content on this website, including written text, logos, images, design elements and branding materials, is the property of Livora Care Pty Ltd unless otherwise stated and is protected by applicable laws.'
  },
  {
    title: 'External Links',
    body:
      'Any links to external websites are provided for convenience and informational purposes only. Livora Care does not control or take responsibility for their content or privacy practices.'
  },
  {
    title: 'Limitation of Liability',
    body:
      'Livora Care will not be liable for any loss or damage arising from the use of this website, reliance on website information, or temporary interruption in website availability.'
  },
  {
    title: 'Governing Law',
    body:
      'These Terms and Conditions are governed by the laws of the State of Victoria, Australia, and any disputes will be subject to the jurisdiction of the courts of Victoria.'
  }
]
</script>

<template>
  <div>
    <PageHero
      badge="Terms & Conditions"
      title="Website Terms and Conditions"
      subtitle="Livora Care Pty Ltd. Last updated: 21 March 2026."
    />

    <section class="section">
      <div class="shell legal-stack">
        <article v-for="section in sections" :key="section.title" class="content-card">
          <h2>{{ section.title }}</h2>
          <p>{{ section.body }}</p>
        </article>

        <article class="content-card">
          <h2>Contact</h2>
          <p>If you have any questions about these Terms and Conditions, you may contact Livora Care directly.</p>
          <p>{{ siteName }} Pty Ltd</p>
          <p>{{ siteLocation }}</p>
          <p>Email: {{ siteEmail }}</p>
          <p>Phone: {{ sitePhone }}</p>
        </article>
      </div>
    </section>
  </div>
</template>
