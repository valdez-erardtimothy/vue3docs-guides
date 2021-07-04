<template>
  <div id="conditionals-and-loops">
    <h1>Conditionals and Loops</h1>
    <div id="conditional-rendering">
      <button class="btn bg-green-400 p-3 m-3" @click="toggleSeen">
        Click this button to see a message!
      </button>
      <p class="p-2" v-if="seen">Now you see me, then what?</p>
    </div>
  </div>
</template>

<style lang="postcss" scoped>
div {
  @apply py-4 bg-gray-200;
}
</style>

<script>
export default {
  name: "ConditionalsAndLoops",
  data() {
    return {
      seen: false,
    };
  },
  methods() {
    return {
      toggleSeen() {
        this.seen != this.seen;
      },
    };
  },
};
</script>
