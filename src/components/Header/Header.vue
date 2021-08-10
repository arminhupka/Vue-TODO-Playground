<template>
  <header class="header">
    <div class="container">
      <h1 class="title">TODO APP</h1>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header"
}
</script>

<style>
.header {
  position: relative;
  height: 35rem;
  display: flex;
  align-items: center;
  background: url("https://picsum.photos/1920/1080") center no-repeat;
  background-size: cover;
}

.header::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: block;
  background: #952ddc;
  opacity: .3;
}

.title {
  position: relative;
  font-size: 7rem;
  color: #fff;
}
</style>