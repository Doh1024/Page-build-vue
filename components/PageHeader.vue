<script setup>
  defineProps({
    pageName: String,
  });
</script>

<template>
  <header class="flex justify-center text-3xl my-3">
    <h1>{{pageName}}</h1>
  </header>
</template>