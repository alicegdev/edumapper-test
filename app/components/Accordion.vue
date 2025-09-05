<template>
  <div class="bg-white rounded-xl shadow-sm overflow-hidden">
    <button
      class="w-full flex justify-between items-center px-4 py-3 text-left font-medium"
      @click="isOpen = !isOpen"
    >
      {{ title }}
      <span class="text-gray-400">{{ isOpen ? "–" : "+" }}</span>
    </button>
    <div v-if="isOpen" class="px-4 pb-4 text-gray-600">
      <slot />
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ title: string }>()

const isOpen = ref(false)
</script>
