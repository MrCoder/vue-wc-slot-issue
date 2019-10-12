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
    // undefined
    console.log(window.App.$slots.default && window.App.$slots.default[0].text);
    this.$nextTick(() => {
      // undefined
      console.log(window.App.$slots.default && window.App.$slots.default[0].text)
    });
    setTimeout(() => {
      // 1234, correct value
      console.log(window.App.$slots.default && window.App.$slots.default[0].text)      
    });
  }
}
</script>
