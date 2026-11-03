<script setup>
defineProps({
  title: { type: String, default: '' },
})
</script>

<template>
  <div class="my-1 rounded-md border bg-gray-100 px-2 py-1 text-center shadow-sm">
    <div v-if="title" class="text-sm font-semibold">{{ title }}</div>
    <slot />
  </div>
</template>
