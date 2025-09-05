<template>
  <div class="bg-white p-4 rounded-xl shadow-sm space-y-3">
    <h3 class="font-medium text-gray-800">{{ title }}</h3>
    <slot />
  </div>
</template>

<script setup lang="ts">
defineProps<{ title: string }>()
</script>
