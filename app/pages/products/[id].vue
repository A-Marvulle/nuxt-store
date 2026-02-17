<template>
  <div>
    <p>Detail Product for: {{ id }}</p>
  </div>
</template>

<script setup>
const { id } = useRoute().params;
</script>
