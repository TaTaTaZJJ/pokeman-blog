<script setup lang="ts">
// https://github.com/vueuse/head
// you can use this to manipulate the document head in any components,
// they will be rendered correctly in the html results with vite-ssg
import { isDark } from '~/composables'

useHead({
  title: 'Ta之境界的博客',
  meta: [
    { name: 'description', content: '口袋人的制作思路，记录及一些心得' },
    {
      name: 'theme-color',
      content: computed(() => isDark.value ? '#00aba9' : '#ffffff'),
    },
  ],
})
</script>

<template>
  <RouterView />
</template>
