<script setup lang="ts">
useHead({
  title: 'Partnering With Referrers | Livora Care'
})

const referralServices = [
  'Supported Independent Living (SIL)',
  'Assistance with Daily Personal Activities',
  'Household Supports',
  'Community Participation',
  'Life Skills Development',
  'Transport Assistance',
  'Group and Centre-Based Activities'
]

const referralBenefits = [
  'Responsive communication',
  'Transparent service delivery',
  'Reliable support staff',
  'Clear documentation and progress updates'
]
</script>

<template>
  <div>
    <PageHero
      badge="Referrers"
      title="Partnering With Support Coordinators and Allied Health Professionals"
      subtitle="Livora Care works collaboratively with referrers to deliver safe, reliable and participant-centred NDIS supports."
    />

    <section class="section">
      <div class="shell split-grid">
        <div class="content-card">
          <h2>Introduction</h2>
          <p>
            We recognise the important role that support coordinators, local area coordinators and allied health
            professionals play in helping participants access the right supports.
          </p>
          <p>
            Our team is committed to responsive communication, reliable service delivery and transparent documentation
            so referrers can feel confident recommending Livora Care.
          </p>
        </div>

        <div class="content-card">
          <h2>Services available for referral</h2>
          <ul class="check-list">
            <li v-for="service in referralServices" :key="service">{{ service }}</li>
          </ul>
        </div>
      </div>
    </section>

    <section class="section soft-section">
      <div class="shell prose-grid">
        <article class="content-card">
          <h2>Our approach to collaborative care</h2>
          <p>
            We work closely with support coordinators and clinicians to ensure supports remain aligned with participant
            goals and clinical recommendations, including behaviour support plans where applicable.
          </p>
        </article>

        <article class="content-card">
          <h2>Governance and quality assurance</h2>
          <p>
            As a registered NDIS provider, Livora Care operates within the NDIS Practice Standards, Code of Conduct,
            incident management frameworks and complaints processes that support safe and accountable delivery.
          </p>
        </article>
      </div>
    </section>

    <section class="section">
      <div class="shell split-grid">
        <div>
          <p class="eyebrow">Referral Process</p>
          <h2>Simple steps from initial conversation to support commencement</h2>
          <p>
            Referrers can contact our team to discuss the participant’s needs, confirm suitability, and arrange an
            initial consultation with the participant and their support network.
          </p>
          <p>
            We then work collaboratively with the referrer to develop an appropriate support arrangement aligned with
            the participant’s NDIS plan.
          </p>
        </div>

        <div class="feature-panel">
          <h3>Working with Livora Care</h3>
          <ul class="check-list">
            <li v-for="item in referralBenefits" :key="item">{{ item }}</li>
          </ul>
          <div class="hero-actions">
            <NuxtLink to="/make-a-referral" class="button button-primary">Submit Referral</NuxtLink>
            <NuxtLink to="/contact" class="button button-secondary">Contact Our Team</NuxtLink>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
