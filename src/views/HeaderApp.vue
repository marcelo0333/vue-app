<template>

  <div class="bg-gray-800 text-white p-4">
    <h1 class="text-2xl font-bold">Header Component</h1>
    <p >This is the header of the application.</p>
    <p >Resize the window to see the console log.</p>
  </div>
</template>

// eslint-disable-next-line vue/block-lang
<script lang="ts" >
export default {
  mounted() {
    window.addEventListener('resize', this.resize());

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

</style>
