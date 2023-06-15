<template>
  <div>
    <h1>users/ {{ $route.params.id }} page </h1>
    <hr>
    <NuxtLink to="/">Top Page</NuxtLink>
  </div>
</template>

<script setup>
definePageMeta({
  validate: async(route) =>{
    return /^\d+$/.test(route.params.id)
    }
})
</script>
