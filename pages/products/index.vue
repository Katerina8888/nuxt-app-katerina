<template>
  <div>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="p in products" :key="p.id">
        <ProductCard :product="p" />
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import type { Data } from '~/types/types'

definePageMeta({
  layout: 'products',
})

// fetch the products
const { data: products } = await useFetch<Data[]>(
  'https://fakestoreapi.com/products'
)

console.log(products.value)
</script>
