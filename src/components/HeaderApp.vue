<template>
  <header class="bg-gray-800 text-white p-4 flex justify-between items-center">
    <slot/>
    <slot name="header">
      <h1 class="text-2xl font-bold">Vulo</h1>
      </slot>
    <slot name="description">
      <h2 class="text-lg"></h2>
      </slot>
    <slot name="title">
      <h1 class="text-2xl font-bold"></h1>
      </slot>
  </header>
</template>

<script >
export default {
  mounted() {
    console.log('mounted', this.$slot());

  },
  beforeUnmount() {
    console.log('beforeUnmount');
    window.removeEventListener('resize', this.resize());

  },
  unmounted() {
    console.log('unmounted');
  },
  methods: {
    resize($event) {
      console.log($event);
    },
  }
}
</script>

<style>
#appH {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
h1 {
  font-size: 2em;
  font-weight: bold;
  color: #ff0000;
}
</style>
