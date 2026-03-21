<script setup lang="ts">
useHead({
  title: 'Our Team | Livora Care'
})

const teamThemes = [
  {
    title: 'Healthcare and Clinical Experience',
    body:
      'Members of the Livora Care leadership team have experience in healthcare and hospital environments, bringing insight into participant wellbeing, safe care practices and collaboration with clinicians.'
  },
  {
    title: 'Biomedical and Research Expertise',
    body:
      'Our team includes professionals with advanced academic and research backgrounds in biomedical science, supporting an evidence-informed approach to quality improvement and service planning.'
  },
  {
    title: 'Pharmaceutical and Healthcare Industry Experience',
    body:
      'Industry experience across therapeutic product development and clinical trials contributes to strong thinking in compliance, risk management and quality assurance.'
  },
  {
    title: 'Corporate Governance and Operational Management',
    body:
      'Leadership experience in corporate and operational governance helps shape structured policies, procedures and quality management frameworks.'
  }
]
</script>

<template>
  <div>
    <PageHero
      badge="Our Team"
      title="A team with diverse professional experience"
      subtitle="Livora Care is supported by a multidisciplinary team with experience across healthcare, disability support, clinical research and organisational management."
    />

    <section class="section">
      <div class="shell">
        <div class="section-heading">
          <h2>Compassionate service delivery backed by strong governance</h2>
          <p>
            The diversity of our team helps ensure that Livora Care maintains both participant-centred care and the
            structured systems needed for high-quality disability services.
          </p>
        </div>
        <div class="card-grid two-up">
          <article v-for="theme in teamThemes" :key="theme.title" class="info-card">
            <h3>{{ theme.title }}</h3>
            <p>{{ theme.body }}</p>
          </article>
        </div>
      </div>
    </section>

    <section class="section soft-section">
      <div class="shell split-grid">
        <div class="content-card">
          <h2>Working together to support participants</h2>
          <p>
            By combining knowledge from healthcare, research, disability services and organisational management, we can
            approach support delivery from multiple perspectives while staying focused on respectful, reliable and
            person-centred supports.
          </p>
        </div>
        <div class="content-card">
          <h2>A culture of continuous learning</h2>
          <p>
            We regularly review service practices, regulatory requirements and emerging sector knowledge so our supports
            remain safe, responsive and aligned with best practice.
          </p>
        </div>
      </div>
    </section>
  </div>
</template>
