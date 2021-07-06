<!-- WIP -->
<template>
  <nav class="sidenav">
    <div class="sidenav-item">
      <p>Introduction</p>
      <div class="sidenav-subitem">
        <router-link to="/">Home</router-link>
      </div>
      <div class="sidenav-subitem">
        <router-link to="/about">About</router-link>
      </div>
      <div class="sidenav-subitem">
        <router-link to="/conditionals-and-loops">
          Conditionals and Loops
        </router-link>
      </div>
    </div>
  </nav>
</template>

<style lang="postcss" scoped>
.sidenav {
  text-align: left;
}
.sidenav .sidenav-item,
.sidenav .sidenav-subitem {
  @apply pt-4 px-5 font-light;
}

/* reconsider design choice later. */
.sidenav .sidenav-link,
.sidenav .sidenav-subitem:hover {
  @apply bg-gray-300 font-medium;
}

.sidenav .sidenav-item .sidenav-subitem {
  @apply pl-4;
}
</style>
