<script setup>
import { RouterView } from 'vue-router'

const navItems = ref([
  {
    id: 1,
    label: 'Review',
  },
  {
    id: 2,
    label: 'Tips',
  },
  {
    id: 3,
    label: 'Alerts',
  },
  {
    id: 4,
    label: 'Blog',
  },
])
</script>

<template>
  <main>
    <TheTopBar :items="navItems" />
    <RouterView />
  </main>
</template>
