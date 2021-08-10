<template>
  <div class="footer-wrapper">
      <p>Tasks: {{length.length}}</p>
  </div>
</template>

<script>
export default {
  name: "Footer",
  props: ["tasks"],
  data() {
    return {
      length: this.tasks
    }
  },
}
</script>

<style>
.footer-wrapper {
  padding: 1rem 2rem;
  background: #fff;
  box-shadow: 0 .4rem 1rem rgba(0,0,0,.3);
}
</style>