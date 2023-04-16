<template>
  <div>
    <p>{{ product.title }}</p>
    <p>{{ product.price }}</p>
    <p>{{ product.id }}</p>
  </div>
</template>

<script setup>
  definePageMeta({ layout: 'products' });
  const { id } = useRoute().params;

  const { data: product } = await useFetch(`https://fakestoreapi.com/products/${id}`);
</script>

<style scoped>

</style>