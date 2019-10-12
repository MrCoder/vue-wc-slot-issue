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
    console.log(window.App.$slots.default && window.App.$slots.default[0].text);
    this.$nextTick(() => {
      console.log(window.App.$slots.default && window.App.$slots.default[0].text)
    });
    setTimeout(() => {
      console.log(window.App.$slots.default && window.App.$slots.default[0].text)      
    });
  }
}
</script>
