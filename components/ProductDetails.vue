<template>
  <div>
    <div class="grid grid-cols-2 gap-10">
      <div class="p-7">
        <img
          :src="product.image"
          alt="product img"
          class="mx-auto my-7 max-w-400px"
        />
      </div>

      <div class="p-7">
        <h2 class="text-4xl my-7">{{ product.title }}</h2>
        <p class="text-xl my-7">Price - ${{ product.price }}</p>
        <h3 class="font-bold border-b-2 mb-4 pb-2">Product description:</h3>
        <p class="mb-7">{{ product.description }}</p>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
const { product } = defineProps(['product'])
</script>
