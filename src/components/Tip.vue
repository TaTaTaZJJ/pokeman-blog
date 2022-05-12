<template>
  <div class="shadow-md p-4 flex flex-row rounded-lg dark:bg-gray-800">
    <div class="bg-teal-500 rounded-lg p-1 mr-1" />
    <b class="p-1 writing-mode-tb">心得</b>
    <p class="p-1">
      <slot />
    </p>
  </div>
</template>

<style>
.writing-mode-tb {
  writing-mode: vertical-lr;
}
</style>
