<template>
  <div class="container">
    <slot />
      <footer>&copy; test.jp</footer>
  </div>
</template>
<style>
.container{
  color: red;
}
footer{
  background-color: orange;
  text-align: center;
  color: white;
}
html{
  /* font-family: 'Permanent Marker', cursive; */
}
</style>