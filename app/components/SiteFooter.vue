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
        <h3 class="footer-links-title">Helpful links</h3>
        <div class="footer-links">
          <NuxtLink v-for="item in footerLinks" :key="item.to" :to="item.to">{{ item.label }}</NuxtLink>
        </div>
      </div>

      <div>
        <h3 class="footer-links-title">Contact</h3>
        <p>{{ sitePhone }}</p>
        <p>{{ siteEmail }}</p>
        <p>{{ siteLocation }}</p>
      </div>
    </div>

    <div class="shell acknowledgement-card">
      <div class="acknowledgement-flags" aria-label="Aboriginal and Torres Strait Islander flags">
        <img src="/aboriginalflag.jpg" alt="Aboriginal flag" class="acknowledgement-flag" />
        <img
          src="/torresstraightislanderflag.jpg"
          alt="Torres Strait Islander flag"
          class="acknowledgement-flag"
        />
      </div>
      <p v-for="statement in acknowledgementStatements" :key="statement">
        {{ statement }}
      </p>
    </div>

    <div class="shell footer-bottom">
      <p>&copy; 2026 Livora Care. Registered NDIS Provider. Serving Greater Melbourne.</p>
    </div>
  </footer>
</template>
