<template>
  <a :href="props.link">
    <button class="p-2 min-h-12 min-w-52 bg-emerald-500 border-2 border-emerald-100 text-emerald-50 text-2xl font-bold transition-all duration-150 hover:bg-emerald-400/90 hover:text-emerald-950 active:scale-90 hover:scale-105 active:border-orange-300 active:bg-orange-500 active:text-orange-950">
      <slot />
    </button>
  </a>
</template>

<script lang="ts" setup>
const props = defineProps(['link'])
</script>