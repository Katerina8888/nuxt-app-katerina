<template>
  <div>
    <p>Product details for {{ id }}</p>
    <div>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Ad doloremque
      aliquam consequatur, suscipit vero porro corrupti cumque nostrum dolorem
      ullam!
    </div>
  </div>
</template>

<script lang="ts" setup>
// obsah závorek musí matchnout název proměnné souboru
const { id } = useRoute().params

definePageMeta({
  layout: 'products',
})
</script>

<style></style>
