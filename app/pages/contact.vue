<script setup lang="ts">
import { siteEmail, siteLocation, sitePhone } from '~/composables/useSiteContent'

useHead({
  title: 'Get in Touch | Livora Care'
})

const enquiryTopics = [
  'Supported Independent Living (SIL)',
  'Daily personal care supports',
  'Community participation supports',
  'Life skills development',
  'Household supports',
  'Transport assistance',
  'Group and centre-based activities',
  'Participant referrals and collaboration opportunities'
]

const faqs = [
  {
    q: 'I’m new to the NDIS. Can Livora Care help me understand how supports work?',
    a: 'Yes. We can explain how supports are delivered, how services are funded under an NDIS plan, and what types of assistance may suit the participant’s goals and daily needs.'
  },
  {
    q: 'Does my family member need to have an NDIS plan before contacting Livora Care?',
    a: 'No. You are welcome to contact us even if the participant is still applying for the NDIS or waiting for plan approval.'
  },
  {
    q: 'How do I know if Livora Care is the right provider for us?',
    a: 'We offer a free initial consultation where we discuss goals, support needs and preferences so you can decide whether our services are the right fit.'
  },
  {
    q: 'Can my family member choose their support workers?',
    a: 'Yes. Participant choice and control are central principles of the NDIS, and we consider language, gender preference, cultural background and experience when matching workers.'
  },
  {
    q: 'What happens after we contact Livora Care?',
    a: 'A member of our team will learn more about the participant’s situation and support needs, then arrange a consultation and service planning if our services are suitable.'
  }
]
</script>

<template>
  <div>
    <PageHero
      badge="Contact"
      title="Get in touch with Livora Care"
      subtitle="Need the right support or want to learn more about our services? Our team is here to help you, your family, or the participant you support."
    />

    <section class="section">
      <div class="shell split-grid top-align">
        <div class="content-card">
          <h2>We are happy to discuss</h2>
          <ul class="check-list">
            <li v-for="topic in enquiryTopics" :key="topic">{{ topic }}</li>
          </ul>
          <div class="contact-meta">
            <p><strong>Phone</strong><br />{{ sitePhone }}</p>
            <p><strong>Email</strong><br />{{ siteEmail }}</p>
            <p><strong>Location</strong><br />{{ siteLocation }}</p>
          </div>
        </div>

        <form class="form-card">
          <h2>Tell us how we can help</h2>
          <p class="muted-copy">
            Please share a brief message about your enquiry or support needs, and a member of our team will contact
            you shortly.
          </p>
          <div class="form-grid">
            <label class="full-span">
              <span>Message</span>
              <textarea rows="6" placeholder="Tell us how we can help"></textarea>
            </label>
            <label>
              <span>Your Name*</span>
              <input type="text" />
            </label>
            <label>
              <span>Your Phone Number*</span>
              <input type="tel" />
            </label>
            <label class="full-span">
              <span>Your Email Address*</span>
              <input type="email" />
            </label>
          </div>
          <button type="button" class="button button-primary">Send Message</button>
          <p class="fine-print">Your information will be kept confidential and used only to respond to your enquiry.</p>
          <p class="fine-print">
            If you are a support coordinator or clinician referring a participant, please visit our
            <NuxtLink to="/make-a-referral">Make a Referral</NuxtLink> page.
          </p>
        </form>
      </div>
    </section>

    <section class="section soft-section">
      <div class="shell">
        <div class="section-heading">
          <p class="eyebrow">Frequently Asked Questions</p>
          <h2>Get your questions answered</h2>
        </div>
        <div class="faq-stack">
          <details v-for="item in faqs" :key="item.q" class="faq-item">
            <summary>{{ item.q }}</summary>
            <p>{{ item.a }}</p>
          </details>
        </div>
        <div class="cta-strip">
          <div>
            <h3>Need to submit a participant referral?</h3>
            <p>Support coordinators and clinicians can send referrals directly through our referral page.</p>
          </div>
          <NuxtLink to="/make-a-referral" class="button button-secondary">Submit a Referral</NuxtLink>
        </div>
      </div>
    </section>
  </div>
</template>
