<script setup lang="ts">
useHead({
  title: 'Supported Independent Living (SIL) in Melbourne | Livora Care'
})

const collaborators = [
  'Support Coordinators',
  'Local Area Coordinators',
  'Occupational Therapists',
  'Behaviour Support Practitioners',
  'Allied Health Professionals'
]

const silPrinciples = [
  'Participant-centred planning shaped by goals, preferences and choices',
  'Safety and wellbeing supported through structured governance and trained staff',
  'Cultural awareness and respect across daily support delivery',
  'Skill development that builds confidence and long-term independence'
]
</script>

<template>
  <div>
    <PageHero
      badge="Supported Independent Living"
      title="Supported Independent Living (SIL) in Melbourne"
      subtitle="Person-centred supported living services designed to help NDIS participants live safely, confidently and independently."
    >
      <div class="hero-actions">
        <NuxtLink to="/contact" class="button button-primary">Book Consultation</NuxtLink>
        <NuxtLink to="/make-a-referral" class="button button-secondary">Refer a Participant</NuxtLink>
      </div>
    </PageHero>

    <section class="section">
      <div class="shell prose-grid">
        <article class="content-card">
          <h2>What is Supported Independent Living?</h2>
          <p>
            Supported Independent Living is an NDIS support that assists participants who require help with daily
            activities while living in a shared or supported home environment.
          </p>
          <p>
            At Livora Care, SIL services are delivered with a strong focus on participant choice, dignity and skill
            development so individuals can live as independently as possible while feeling safe and supported.
          </p>
        </article>

        <article class="content-card">
          <h2>How Livora Care supports participants in SIL</h2>
          <p>
            Our support workers assist with personal care, meal preparation, household tasks and community engagement
            while also helping participants develop practical skills that promote long-term independence.
          </p>
          <p>
            Each SIL arrangement is tailored to the individual and reflects their goals, cultural preferences and
            support needs.
          </p>
        </article>
      </div>
    </section>

    <section class="section soft-section">
      <div class="shell split-grid">
        <div class="content-card">
          <h2>24-hour support structure</h2>
          <p>
            Depending on participant needs, SIL supports may be delivered across a structured 24-hour roster.
            Morning supports focus on preparing for the day, afternoons and evenings on household activities and
            community engagement, and overnight support is available where required.
          </p>
        </div>

        <div class="content-card">
          <h2>Collaboration with support teams</h2>
          <p>
            Successful SIL arrangements depend on close coordination between participants, families and professional
            support teams.
          </p>
          <ul class="check-list">
            <li v-for="item in collaborators" :key="item">{{ item }}</li>
          </ul>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="shell split-grid">
        <div>
          <p class="eyebrow">Our Approach to SIL</p>
          <h2>Structured support guided by dignity, safety and choice</h2>
          <ul class="check-list">
            <li v-for="item in silPrinciples" :key="item">{{ item }}</li>
          </ul>
        </div>

        <div class="feature-panel">
          <h3>Who can benefit from SIL?</h3>
          <p>
            SIL may be suitable for NDIS participants who require regular assistance with daily living and who would
            benefit from a supported environment that strengthens independence and community connection.
          </p>
          <h3>Why support coordinators choose Livora Care</h3>
          <p>
            We focus on reliable supports, clear communication and collaborative practice aligned with the NDIS
            Practice Standards and Code of Conduct.
          </p>
        </div>
      </div>
    </section>
  </div>
</template>
