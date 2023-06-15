<template>
  <div>
    <NuxtLayout>
      <NuxtPage></NuxtPage>
    </NuxtLayout>
  </div>
</template>

<script setup>
  useHead({
    title: "Nuxt 3 user",
    link:[
      {
        rel: "stylesheet" , href: "https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500&family=Noto+Serif+JP:wght@300;400;500;700&family=Permanent+Marker&display=swap"
      }
    ]
  })
  const { data: users } = await useFetch('https://jsonplaceholder.typicode.com/users')
</script>