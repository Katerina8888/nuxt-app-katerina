<template>
  <div>
    <div class="mt-7 max-w-sm mx-auto text-center card">
      <p class="mt-7 text-7xl font-bold">{{ error!.statusCode }}</p>
      <p class="mt-7 text-6xl">Oooops.</p>
      <p class="mt-7">{{ error!.message }}</p>
      <button @click="handleError" class="btn my-7">Go Home...</button>
    </div>
  </div>
</template>

<script setup lang="ts">
import type { NuxtError } from '#app'

const props = defineProps({
  error: Object as () => NuxtError,
})

const handleError = () => clearError({ redirect: '/' })
</script>
