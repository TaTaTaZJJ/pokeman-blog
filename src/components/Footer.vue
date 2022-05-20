<script setup lang="ts">
import { toggleDark } from '~/composables'
</script>

<template>
  <div flex justify-center mt-10>
    <span>2022 &copy; Ta之境界</span>
    <button class="icon-btn mx-2 !outline-none" title="黑暗模式" @click="toggleDark()">
      <div i="carbon-sun dark:carbon-moon" />
    </button>
  </div>
</template>
