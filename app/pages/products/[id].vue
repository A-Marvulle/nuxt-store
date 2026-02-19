<template>
  <div>
    <Head>
      <Title>Nuxt Fake Store | {{ product.title }}</Title>
      <Meta name="description" :content="product.description" />
    </Head>

    <ProductDetail :product="product" />
  </div>
</template>

<script setup>
const { id } = useRoute().params;
const urlId = "https://fakestoreapi.com/products/" + id;

const { data: product } = await useFetch(urlId, { key: id });

if (!product.value) {
  throw createError({
    statusCode: 404,
    statusMessage: "Product not found",
    fatal: true,
  });
}

definePageMeta({ layout: "products" });
</script>
