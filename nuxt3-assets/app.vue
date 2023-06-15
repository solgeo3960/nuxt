<template>
  <div>
   <h1> {{ counter }}</h1>
   <button @click="counterStore.countUp">+</button>
   <button @click="counterStore.countDown">-</button>
   <button @click="counterStore.Reset">Reset</button>
  </div>
</template>

<script setup>
  const counterStore = useCounterState()
  const { counter} = counterStore
</script>