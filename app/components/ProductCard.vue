<template>
  <div>
    <div class="card text-center">
      <img :src="`${product.image}`" :title="`Cover ${product.title}`" :alt="`Cover ${product.title}`" class="thumb" />
      <h3 class="font-bold text-gray-500 m-4 truncate">{{ product.title }}</h3>
      <NuxtLink :to="`/products/${product.id}`" class="btn my-4">
        View Details
      </NuxtLink>
    </div>
  </div>
</template>

<script setup>
const { product } = defineProps(["product"]);
</script>

<style scoped>
.thumb {
  height: 120px;
  width: 70%;
  object-fit: contain;
  margin: 0 auto;
}
</style>
