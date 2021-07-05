<!--<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div>
  <router-view />
</template>-->

<template>
  <div class="flex flex-row flex-wrap">
    <aside class="flex-none items-center justify-center mx-4">
      <VerticalNav />
    </aside>
    <main class="flex-1 bg-gray-200 py-12">
      <router-view />
    </main>
  </div>
</template>
<style>
/* default, included on build */
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>

<script>
import VerticalNav from "./components/VerticalNav";
export default {
  components: {
    VerticalNav,
  },
};
</script>
