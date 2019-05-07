<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <button v-on:click="reverseMessage">Reverse Message</button>
    <ol>
      <li v-for="todo in todos">
        {{ todo.text }}
      </li>
    </ol>
    <p>Whatup</p>
    <p>Number of contributers: {{ numPeople }}</p>
    <button v-on:click="makeDonation">Add donation</button>
  </div>
</template>

<style></style>

<script>
export default {
  data: function() {
    return {
      message: "Welcome to Vue.js!",
      todos: [{ text: "Learn JavaScript" }, { text: "Learn Vue" }, { text: "Build something awesome" }],
      numPeople: 0
    };
  },
  created: function() {},
  methods: {
    reverseMessage: function() {
      this.message = this.message
        .split("")
        .reverse()
        .join("");
    },
    makeDonation: function() {
      console.log("make donation", this.todos);
      this.numPeople += 1;
    }
  }
};
</script>
