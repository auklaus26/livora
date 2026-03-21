<script setup lang="ts">
import { siteEmail, siteLocation, siteName, sitePhone } from '~/composables/useSiteContent'

useHead({
  title: 'Privacy Policy | Livora Care'
})

const sections = [
  {
    title: 'Our Commitment to Privacy',
    body:
      'Livora Care recognises that privacy and confidentiality are essential components of respectful and ethical service delivery. Our practices are guided by the Privacy Act 1988 (Cth) and the Australian Privacy Principles.'
  },
  {
    title: 'Collection of Personal Information',
    body:
      'We may collect personal information through website contact forms, referral submissions, enquiries and feedback channels where that information is reasonably necessary to respond or provide assistance.'
  },
  {
    title: 'Use of Personal Information',
    body:
      'Personal information may be used to respond to enquiries, communicate regarding services, process referrals or feedback, and improve how our organisation delivers services and communicates with the community.'
  },
  {
    title: 'Disclosure of Personal Information',
    body:
      'Livora Care does not sell or trade personal information. Information may only be shared with authorised staff members or service partners where necessary to respond to enquiries, facilitate coordination or comply with legal obligations.'
  },
  {
    title: 'Website Data and Analytics',
    body:
      'The website may collect limited anonymous technical data, such as browser type or pages visited, to improve functionality and accessibility.'
  },
  {
    title: 'Data Security',
    body:
      'We take appropriate steps to safeguard personal information against misuse, loss or unauthorised access, while recognising that no internet transmission can be guaranteed to be completely secure.'
  },
  {
    title: 'Access and Correction',
    body:
      'Individuals may request access to personal information held about them and request corrections where needed. We will take reasonable steps to respond in a timely and respectful manner.'
  },
  {
    title: 'Privacy Concerns or Complaints',
    body:
      'If concerns cannot be resolved through Livora Care, individuals may seek further assistance from the Office of the Australian Information Commissioner (OAIC).'
  },
  {
    title: 'Updates to This Policy',
    body:
      'This Privacy Policy may be updated from time to time to reflect changes in legislation, organisational practices or website functionality.'
  }
]
</script>

<template>
  <div>
    <PageHero
      badge="Privacy Policy"
      title="Privacy Policy"
      subtitle="Livora Care Pty Ltd. Last updated: 21 March 2026."
    />

    <section class="section">
      <div class="shell legal-stack">
        <article v-for="section in sections" :key="section.title" class="content-card">
          <h2>{{ section.title }}</h2>
          <p>{{ section.body }}</p>
        </article>

        <article class="content-card">
          <h2>Contact Information</h2>
          <p>{{ siteName }} Pty Ltd</p>
          <p>{{ siteLocation }}</p>
          <p>Email: {{ siteEmail }}</p>
          <p>Phone: {{ sitePhone }}</p>
        </article>
      </div>
    </section>
  </div>
</template>
