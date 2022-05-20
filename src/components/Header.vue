<template>
  <nav>
    <div class="prose flex flex-wrap justify-between item-center mx-auto">
      <h1>
        Ta之境界的技术博客
      </h1>
      <div class="flex justify-between item-center">
        <router-link to="/">
          主页
        </router-link>
        <router-link to="/concept">
          概念
        </router-link>
        <router-link to="/getting-started">
          入门
        </router-link>
        <router-link to="/tutorial">
          教学
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
