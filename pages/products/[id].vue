<template>
  <div v-if="product">
    <p>{{ product.title }}</p>
    <p>{{ product.price }}</p>
    <p>{{ product.id }}</p>
  </div>
  <div v-else>
    <p>Loading...</p>
  </div>
</template>

<script lang="ts" setup>
import type { Data } from '~/types/types'

// obsah závorek musí matchnout název proměnné souboru
const { id } = useRoute().params
const uri = 'https://fakestoreapi.com/products/' + id

//fetch the product
const { data: product } = await useFetch<Data>(uri)

definePageMeta({
  layout: 'products',
})
</script>

<style></style>
