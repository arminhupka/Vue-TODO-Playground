<template>
  <div class="add-task-wrapper">
    <input ref="taskInput" @input="handleInput" type="text" placeholder="New task description...">
    <button @click="addTask(), cleanInput()">ADD TASK</button>
  </div>
</template>

<script>
export default {
  name: "Add Task",
  props: ["addTask", "handleInput"],
  methods: {
    cleanInput() {
      this.$refs['taskInput'].value=""
    }
  },
  mounted() {
    window.addEventListener('keydown', (e) => {
      if(e.key === 'Enter') {
        this.addTask();
        this.cleanInput();
      }
    })
  }
}
</script>

<style>
  .add-task-wrapper {
    padding: 2rem;
    margin-top: -5rem;
    margin-bottom: 2rem;
    display: flex;
    background: #fff;
    box-shadow: 0 .4rem 1rem rgba(0,0,0,.3);
  }

  input {
    flex: 1;
    margin-right: 2rem;
    border: none;
    border-bottom: .1rem solid #dedede;
  }

  input:focus {
    outline: none;
  }

  button {
    flex: 0 1 auto;
    padding: 1rem 2rem;
    font-weight: bold;
    color: #fff;
    background: #952ddc;
    border: none;
  }
</style>