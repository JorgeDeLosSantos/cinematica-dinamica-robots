<script setup>
import { computed } from 'vue'

const props = defineProps({
  type: { type: String, default: 'note' },
  title: { type: String, default: '' },
})

const config = computed(() => {
  const variants = {
    note: { icon: 'ℹ️', border: 'border-blue-500', bg: 'bg-blue-50', text: 'text-blue-900', title: 'Nota' },
    tip: { icon: '💡', border: 'border-green-500', bg: 'bg-green-50', text: 'text-green-900', title: 'Idea clave' },
    warning: { icon: '⚠️', border: 'border-orange-500', bg: 'bg-orange-50', text: 'text-orange-900', title: 'Advertencia' },
    important: { icon: '❗', border: 'border-red-500', bg: 'bg-red-50', text: 'text-red-900', title: 'Importante' },
  }
  return variants[props.type] ?? variants.note
})
</script>

<template>
  <div class="my-4 rounded border-l-4 px-5 py-4" :class="[config.border, config.bg, config.text]">
    <div class="mb-2 font-bold">
      <span class="mr-2">{{ config.icon }}</span>{{ title || config.title }}
    </div>
    <div><slot /></div>
  </div>
</template>
