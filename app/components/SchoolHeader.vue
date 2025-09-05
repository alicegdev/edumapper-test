<template>
  <div
    class="rounded-xl p-4 text-white flex justify-between items-center w-[720px] h-[88px]"
    :class="gradient"
  >
    <div>
      <h2 class="font-bold text-lg">{{ name }}</h2>
      <p class="text-sm opacity-90">{{ city }} · {{ type }}</p>
    </div>
    <button
      class="bg-white text-gray-800 px-3 py-1 rounded-full text-sm font-medium shadow hover:bg-gray-50"
    >
      Modifier
    </button>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  name: string
  city: string
  type: string
  gradient?: string
}>()

// Gradient par défaut
const gradient = "bg-gradient-to-r from-orange-500 to-purple-500"
</script>
