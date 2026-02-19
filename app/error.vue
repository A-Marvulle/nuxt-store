<template>
  <NuxtLayout name="default">
    <div class="mt-7 max-w-sm mx-auto text-center card">
      <p class="mt-7 text-7xl font-bold">{{ error.statusCode }}</p>
      <p class="mt-7 text-6xl">Ooops.</p>
      <p class="mt-7">{{ error.message }}</p>
      <div>
        <button class="btn my-7" @click="handleError">Go Home...</button>
      </div>
    </div>
  </NuxtLayout>
</template>

<script setup>
defineProps({
  error: Object,
});

const handleError = () => clearError({ redirect: "/" });
</script>
