<template>
  <div id="conditionals-and-loops">
    <h1>Conditionals and Loops</h1>
    <div id="conditional-rendering">
      <button class="btn bg-green-400 p-3 m-3" @click="toggleSeen">
        Click this button to see a message!
      </button>
      <p class="p-2" v-if="seen">Now you see me, then what?</p>
    </div>
    <div id="list-rendering" class="text-left">
      <h1 class="text-center">List Rendering</h1>
      <ul>
        <li class="px-2 py-3" :key="todo.id" v-for="todo in todos">
          {{ todo.text }}
        </li>
      </ul>
    </div>
    <div id="through-bind"></div>
  </div>
</template>

<style lang="postcss" scoped>
div {
  @apply py-4;
}
div > div {
  @apply py-4 my-1 border-b-4 border-gray-700 border-opacity-25;
}
</style>

<script>
export default {
  name: "ConditionalsAndLoops",
  data() {
    return {
      seen: false,
      todos: [
        { id: 1, text: "Learn JavaScript" },
        { id: 2, text: "Learn Vue" },
        { id: 3, text: "Build something awesome" },
      ],
    };
  },
  methods: {
    toggleSeen() {
      this.seen = !this.seen;
    },
  },
};
</script>
