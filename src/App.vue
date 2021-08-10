<template>
  <Header/>
  <ToDo v-bind:tasks="tasks" v-bind:addTask="addTask" v-bind:handleInput="handleInput"/>
</template>

<script>
import Header from "./components/Header/Header";
import ToDo from "./components/ToDo/ToDo";

export default {
  name: 'App',
  components: {
    Header,
    ToDo,
  },
  data() {
    return {
      newTask: "",
      tasks: ["First Task", "Second Task"]
    }
  },
  methods: {
    addTask() {
      if (!this.newTask) {
        return;
      }
      this.tasks.push(this.newTask)
    },
    handleInput(e) {
      this.newTask = e.target.value;
    }
  }
}
</script>

<style>
*, *::before, *::after {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

html {
  font-size: 62.5%;
}

body {
  font-size: 1.4rem;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #333;
}

.container {
  width: 100%;
  max-width: 122rem;
  margin: 0 auto;
  padding: 0 2.4rem;
}
</style>
