<script setup lang="ts">
defineProps<{
  title: string
  subtitle: string
  badge?: string
}>()
</script>

<template>
  <section class="page-hero">
    <div class="shell">
      <div class="page-hero-panel">
        <p v-if="badge" class="eyebrow">{{ badge }}</p>
        <h1>{{ title }}</h1>
        <p class="lead">{{ subtitle }}</p>
        <slot />
      </div>
    </div>
  </section>
</template>
