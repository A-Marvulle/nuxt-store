<template>
  <div>
    <p>{{ product.title }}</p>
    <p>{{ product.price }}</p>
    <p>{{ product.id }}</p>
  </div>
</template>

<script setup>
  const { id } = useRoute().params
  const urlId = 'https://fakestoreapi.com/products/' + id
  const { data: product } = await useFetch(urlId, { key: id })

  definePageMeta({layout: "products"})
</script>