<template>
  <div>
    <h1>Top page</h1>
    <hr>
    <NuxtLink to="/price">Price</NuxtLink>
    <br>
    <NuxtLink to="/mypage">mypage</NuxtLink>
    <br>
    <NuxtLink to="/users">users</NuxtLink>
    <p>{{ users[0].id }}{{ users[0].name }}</p>
    <ul>
      <li v-for="user in users" :key="user.id">
        {{ user.id }},{{ user.name }}
      </li>
    </ul>
  </div>
</template>

<script setup>

  const { data: users , error } = await useFetch('https://jsonplaceholder.typicode.com/users')
  // console.log(error)
  if (error.value) {
  throw createError({ statusCode:404, statusMessage: 'page not found!!'})    
  }
</script>