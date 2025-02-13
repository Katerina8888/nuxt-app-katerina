<template>
  <div>
    <p>Product details for {{ id }}</p>
    <div class="bg-red-500">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Ad doloremque
      aliquam consequatur, suscipit vero porro corrupti cumque nostrum dolorem
      ullam!
    </div>
  </div>
</template>

<script lang="ts" setup>
// obsah závorek musí matchnout název proměnné souboru
const { id } = useRoute().params
// const uri = 'https://fakestoreapi.com/products' + id

//fetch the product
// const { data: product }

definePageMeta({
  layout: 'products',
})
</script>

<style></style>
