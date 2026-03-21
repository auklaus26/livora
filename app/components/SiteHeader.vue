<script setup lang="ts">
import { primaryNav } from '~/composables/useSiteContent'
</script>

<template>
  <header class="site-header">
    <div class="shell header-inner">
      <div class="topbar">
        <NuxtLink to="/" class="brand-mark">
          <img src="/logo.png" alt="Livora Care logo" class="brand-logo" />
        </NuxtLink>
      </div>

      <nav class="main-nav" aria-label="Primary">
        <NuxtLink
          v-for="item in primaryNav"
          :key="item.to"
          :to="item.to"
          class="nav-link"
          active-class="nav-link-active"
        >
          {{ item.label }}
        </NuxtLink>
      </nav>

      <div class="topbar-actions">
        <NuxtLink to="/make-a-referral" class="button button-secondary">Referrals</NuxtLink>
        <NuxtLink to="/contact" class="button button-primary">Book Consultation</NuxtLink>
      </div>
    </div>
  </header>
</template>
