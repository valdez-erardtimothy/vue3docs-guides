<template>
  <div class="home mx-auto py-2">
    <img class="mx-auto" alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <ClockWidget />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import ClockWidget from "@/components/ClockWidget.vue";

export default {
  name: "Home",
  components: {
    HelloWorld,
    ClockWidget,
  },
};
</script>
