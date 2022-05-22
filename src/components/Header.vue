<script lang="ts" setup>
defineProps<{
  title: string
  routes: { title: string; route: string }[]
}>()
</script>

<template>
  <nav>
    <div class="prose flex flex-wrap justify-between item-center mx-auto">
      <h1>
        {{ title }}
      </h1>
      <div class="flex justify-between item-center">
        <router-link v-for="{ route, title: name } in routes" :key="route" :to="route">
          {{ name }}
        </router-link>
      </div>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
h1 {
  margin: 0 !important;
}

a {
  text-decoration: none !important;
  font-size: 24px;

  &:not(:first-child) {
    margin-left: 10px;
  }

  &:not(:last-child) {
    margin-right: 10px;
  }
}
</style>
