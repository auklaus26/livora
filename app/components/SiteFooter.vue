<script setup lang="ts">
import {
  acknowledgementStatements,
  footerLinks,
  siteEmail,
  siteLocation,
  siteName,
  sitePhone
} from '~/composables/useSiteContent'
</script>

<template>
  <footer class="site-footer">
    <div class="shell footer-grid">
      <div>
        <p class="eyebrow">Reliable disability supports across Melbourne</p>
        <h2>{{ siteName }}</h2>
        <p class="muted-copy">
          Person-centred NDIS disability supports focused on independence, safety and respectful care.
        </p>
      </div>

      <div>
        <h3>Helpful links</h3>
        <div class="footer-links">
          <NuxtLink v-for="item in footerLinks" :key="item.to" :to="item.to">{{ item.label }}</NuxtLink>
        </div>
      </div>

      <div>
        <h3>Contact</h3>
        <p>{{ sitePhone }}</p>
        <p>{{ siteEmail }}</p>
        <p>{{ siteLocation }}</p>
      </div>
    </div>

    <div class="shell acknowledgement-card">
      <p v-for="statement in acknowledgementStatements" :key="statement">
        {{ statement }}
      </p>
    </div>

    <div class="shell footer-bottom">
      <p>NDIS Registered Provider</p>
      <p>Melbourne Service Area</p>
      <p>Participant Rights</p>
      <p>Complaints & Feedback</p>
      <p>Privacy Policy</p>
      <p>Social links can be added once final accounts are confirmed.</p>
    </div>
  </footer>
</template>
