<template>
  <layout-default>
    <router-view></router-view>
  </layout-default>
</template>

<script setup lang="ts">
import LayoutDefault from '@/components/layouts/LayoutDefault.vue'
</script>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
