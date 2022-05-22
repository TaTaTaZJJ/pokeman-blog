<script lang="ts" setup>
const routes = [
  { title: '主页', route: '/' },
  { title: '概念', route: '/concept' },
  { title: '入门', route: '/getting-started' },
  { title: '教学', route: '/tutorial' },
]
</script>

<template>
  <main px-4 py-10 text-center text-gray-700 dark:text-gray-200>
    <Header :routes="routes" title="口袋人" />
    <RouterView />
    <Footer />
  </main>
</template>
