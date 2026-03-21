<script setup lang="ts">
useHead({
  title: 'Livora Care | Supported Independent Living & NDIS Disability Support Melbourne',
  meta: [
    {
      name: 'description',
      content:
        'Livora Care provides Supported Independent Living and person-centred NDIS disability supports across Melbourne.'
    }
  ]
})

const services = [
  {
    title: 'Supported Independent Living (SIL)',
    body:
      'Structured supports that assist participants to live safely and independently in a shared or supported home environment.'
  },
  {
    title: 'Daily Personal Care',
    body: 'Respectful assistance with personal routines, mobility and everyday activities.'
  },
  {
    title: 'Household Supports',
    body: 'Help with maintaining a safe and organised home, including cleaning, meal preparation and laundry.'
  },
  {
    title: 'Community Participation',
    body: 'Support to access social, recreational and community activities.'
  },
  {
    title: 'Life Skills Development',
    body: 'Building practical skills such as budgeting, cooking and communication.'
  },
  {
    title: 'Transport Assistance',
    body: 'Support to attend appointments, community activities and daily commitments.'
  }
]

const strengths = [
  'Participant dignity and choice',
  'Reliable and responsive service delivery',
  'Collaborative work with support coordinators and clinicians',
  'Continuous improvement of our supports'
]

const compliance = [
  'NDIS Practice Standards',
  'NDIS Code of Conduct',
  'Quality and Safeguards Commission requirements',
  'Participant safeguarding and incident management frameworks'
]
</script>

<template>
  <div>
    <section class="hero-section">
      <div class="shell hero-grid">
        <div>
          <p class="eyebrow">Supported Independent Living & NDIS Disability Supports in Melbourne</p>
          <h1>Reliable disability supports built around independence, safety and meaningful daily life.</h1>
          <p class="lead">
            Livora Care is a registered NDIS provider delivering person-centred disability supports tailored to each
            participant’s goals, preferences and support needs.
          </p>
          <div class="hero-actions">
            <NuxtLink to="/contact" class="button button-primary">Book Free Consultation</NuxtLink>
            <NuxtLink to="/make-a-referral" class="button button-secondary">Refer a Participant</NuxtLink>
          </div>
        </div>

        <div class="hero-card-stack">
          <article class="spotlight-card">
            <p class="card-label">Welcome to Livora Care</p>
            <h2>Professional disability supports across Melbourne</h2>
            <p>
              We help participants live as independently as possible with tailored support for daily activities, life
              skills and community participation.
            </p>
          </article>

          <article class="mini-callout">
            <span class="mini-callout-label">Working with participants, families and referrers</span>
            <p>Responsive communication, careful planning and consistent service delivery.</p>
          </article>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="shell">
        <div class="section-heading">
          <p class="eyebrow">NDIS Services We Provide</p>
          <h2>Supports designed for daily living, independence and community engagement</h2>
        </div>
        <div class="card-grid three-up">
          <article v-for="service in services" :key="service.title" class="info-card">
            <h3>{{ service.title }}</h3>
            <p>{{ service.body }}</p>
          </article>
        </div>
      </div>
    </section>

    <section class="section soft-section">
      <div class="shell split-grid">
        <div>
          <p class="eyebrow">Supported Independent Living (SIL)</p>
          <h2>Structured support in a safe and supportive home environment</h2>
          <p>
            Our SIL supports assist with daily routines, household responsibilities, personal care and community
            engagement while encouraging skill development and confidence.
          </p>
          <p>
            Each SIL arrangement is tailored to the participant’s goals and delivered in collaboration with support
            coordinators, families and allied health professionals.
          </p>
          <NuxtLink to="/supported-independent-living" class="text-link">Learn more about SIL</NuxtLink>
        </div>

        <div class="feature-panel">
          <h3>Why participants and referrers choose Livora Care</h3>
          <p>
            Livora Care combines professional governance, experienced support staff and participant-centred care to
            deliver reliable disability supports.
          </p>
          <ul class="check-list">
            <li v-for="item in strengths" :key="item">{{ item }}</li>
          </ul>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="shell split-grid">
        <div class="feature-panel">
          <p class="eyebrow">For Support Coordinators & Referrers</p>
          <h2>Collaboration with clear communication and consistent service delivery</h2>
          <p>
            We work closely with support coordinators, local area coordinators, occupational therapists, behaviour
            support practitioners and other allied health professionals to ensure supports remain aligned with each
            participant’s plan and goals.
          </p>
          <NuxtLink to="/referrers" class="button button-secondary">Submit a Referral</NuxtLink>
        </div>

        <div class="consult-card">
          <p class="eyebrow">Start With a Free Consultation</p>
          <h3>Choosing the right provider should start with a real conversation.</h3>
          <p>
            We offer a free initial consultation to help participants, families and referrers discuss support needs,
            explore services and determine the most appropriate support arrangement.
          </p>
          <NuxtLink to="/contact" class="button button-primary">Book a Consultation</NuxtLink>
        </div>
      </div>
    </section>

    <section class="section soft-section">
      <div class="shell split-grid">
        <div>
          <p class="eyebrow">A Registered NDIS Provider You Can Trust</p>
          <h2>Governance systems designed for safe, transparent and accountable service delivery</h2>
          <ul class="check-list">
            <li v-for="item in compliance" :key="item">{{ item }}</li>
          </ul>
        </div>

        <div class="contact-panel">
          <h3>Contact Livora Care</h3>
          <p>
            Whether you are a participant, family member or support coordinator, we welcome the opportunity to discuss
            your support needs.
          </p>
          <div class="hero-actions">
            <NuxtLink to="/contact" class="button button-primary">Contact Us</NuxtLink>
            <NuxtLink to="/make-a-referral" class="button button-secondary">Refer a Participant</NuxtLink>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
