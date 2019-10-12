<template>
  <div id="app">
    <slot></slot>
  </div>
</template>

<script>

export default {
  name: 'app',
  mounted() {
    window.App = this;
    console.log(this.$slots);
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
