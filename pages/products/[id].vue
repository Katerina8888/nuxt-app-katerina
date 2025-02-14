<template>
  <ProductDetails :product="product" />
</template>

<script lang="ts" setup>
import type { Data } from '~/types/types'

// obsah závorek musí matchnout název proměnné souboru
const { id } = useRoute().params
const uri = 'https://fakestoreapi.com/products/' + id

//fetch the product
const { data: product } = await useFetch<Data>(uri)

if (!product.value) {
  throw createError({ statusCode: 404, statusMessage: 'Product not found' })
}

definePageMeta({
  layout: 'products',
})
</script>
