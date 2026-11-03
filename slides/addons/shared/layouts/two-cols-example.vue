<template>
  <div class="slidev-layout two-cols-example grid h-full grid-cols-2 gap-10">
    <div class="pr-4">
      <slot />
    </div>
    <div class="border-l-4 border-gray-300 pl-4">
      <slot name="right" />
    </div>
  </div>
</template>
