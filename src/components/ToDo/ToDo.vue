<template>
  <div class="todo container">
    <AddTask v-bind:addTask="addTask" v-bind:handleInput="handleInput"/>
    <TaskList v-bind:tasksArr="tasksArr"/>
    <Footer v-bind:tasks="tasksArr"/>
  </div>
</template>

<script>
import AddTask from "../AddTask/AddTask";
import TaskList from "../TaskList/TaskList";
import Footer from "../Footer/Footer";

export default {
  name: "ToDO",
  props: ['tasks', 'addTask', 'handleInput'],
  data() {
    return {
      tasksArr: this.tasks
    }
  },
  components: {
    Footer,
    AddTask,
    TaskList
  }
}
</script>

<style>
.todo {
  position: relative;
  margin-top: -10rem;
  z-index: 2;
}
</style>