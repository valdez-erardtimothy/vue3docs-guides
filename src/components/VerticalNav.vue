<template>
  <nav class="sidenav">
    <p class="sidenav-item"><router-link to="/">Home</router-link></p>
    <p class="sidenav-item"><router-link to="/about">About</router-link></p>
    <p class="sidenav-item">
      <router-link to="/conditionals-and-loops">
        Conditionals and Loops
      </router-link>
    </p>
  </nav>
</template>

<style lang="postcss" scoped>
.sidenav > .sidenav-item {
  @apply py-4 px-5 font-light;
}
.sidenav > .sidenav-item:hover {
  @apply bg-gray-300 font-medium;
}
</style>
