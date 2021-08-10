<template>
  <div class="tasks-list-wrapper">
    <ul class="tasks-list">
      <li class="tasks-item" v-for="task in tasks" :key="task">{{task}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Task List",
  props: ['tasksArr'],
  data() {
    return {
      tasks: this.tasksArr
    }
  }
}
</script>

<style>
.tasks-list-wrapper {
  margin-bottom: 2rem;
  display: flex;
  background: #fff;
  box-shadow: 0 .4rem 1rem rgba(0,0,0,.3);
}

.tasks-list {
  width: 100%;
  list-style: none;
}

.tasks-item {
  padding: 2rem;
  font-weight: bold;
  border-bottom: .1rem solid #dedede;
}

.tasks-item:last-child {
  border-bottom: none;
}

.tasks-item:hover {
  background: #f5f5f5;
}

</style>