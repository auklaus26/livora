<script setup lang="ts">
useHead({
  title: 'Why Choose Livora Care'
})

const reasons = [
  'Participant-centred support that respects individual goals, preferences and cultural background',
  'Strong governance and quality systems covering safeguarding, incident management and complaints handling',
  'Healthcare, research and operational leadership experience informing safe and accountable service delivery',
  'Collaborative relationships with families, support coordinators and allied health professionals',
  'Continuous improvement that responds to participant and referrer feedback'
]
</script>

<template>
  <div>
    <PageHero
      badge="Why Choose Livora Care"
      title="A trusted and responsible NDIS provider"
      subtitle="Choosing a disability support provider is an important decision. Livora Care aims to provide services that are reliable, respectful and aligned with each participant’s needs."
    />

    <section class="section">
      <div class="shell split-grid">
        <div>
          <p class="eyebrow">Participant-Centred Support</p>
          <h2>Supports shaped around dignity, independence and meaningful participation</h2>
          <p>
            We work closely with participants and their support networks to develop arrangements that respect personal
            choice while encouraging confidence in everyday life.
          </p>
        </div>
        <div class="feature-panel">
          <h3>Why Livora Care stands out</h3>
          <ul class="check-list">
            <li v-for="reason in reasons" :key="reason">{{ reason }}</li>
          </ul>
        </div>
      </div>
    </section>

    <section class="section soft-section">
      <div class="shell split-grid">
        <div class="content-card">
          <h2>Supporting independence and quality of life</h2>
          <p>
            Our goal is to help participants live as independently as possible while feeling supported and respected in
            their daily lives through reliable supports, collaborative care and participant-centred planning.
          </p>
        </div>
        <div class="consult-card">
          <h3>Start a conversation with our team</h3>
          <p>
            If you are a participant, family member or support coordinator exploring disability support services, we
            welcome the opportunity to discuss your needs.
          </p>
          <div class="hero-actions">
            <NuxtLink to="/contact" class="button button-primary">Contact Livora Care</NuxtLink>
            <NuxtLink to="/contact" class="button button-secondary">Book a Consultation</NuxtLink>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
