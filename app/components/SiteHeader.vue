<script setup lang="ts">
import { ref } from 'vue'
import { primaryNav } from '~/composables/useSiteContent'

const isMenuOpen = ref(false)

const closeMenu = () => {
  isMenuOpen.value = false
}
</script>

<template>
  <header class="site-header">
    <div class="shell header-inner">
      <div class="topbar">
        <NuxtLink to="/" class="brand-mark">
          <img src="/logo.png" alt="Livora Care logo" class="brand-logo" />
        </NuxtLink>

        <button
          type="button"
          class="menu-toggle"
          :aria-expanded="isMenuOpen ? 'true' : 'false'"
          aria-controls="site-menu"
          :aria-label="isMenuOpen ? 'Close navigation menu' : 'Open navigation menu'"
          @click="isMenuOpen = !isMenuOpen"
        >
          <span class="menu-toggle-box" aria-hidden="true">
            <span class="menu-toggle-line"></span>
            <span class="menu-toggle-line"></span>
            <span class="menu-toggle-line"></span>
          </span>
        </button>
      </div>

      <div id="site-menu" class="header-nav" :class="{ 'is-open': isMenuOpen }">
        <nav class="main-nav" aria-label="Primary">
          <NuxtLink
            v-for="item in primaryNav"
            :key="item.to"
            :to="item.to"
            class="nav-link"
            active-class="nav-link-active"
            @click="closeMenu"
          >
            {{ item.label }}
          </NuxtLink>
        </nav>

        <div class="topbar-actions">
          <NuxtLink to="/make-a-referral" class="button button-secondary" @click="closeMenu">Referrals</NuxtLink>
          <NuxtLink to="/contact" class="button button-primary" @click="closeMenu">Book Consultation</NuxtLink>
        </div>
      </div>
    </div>
  </header>
</template>
