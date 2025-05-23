<template>
  <header class="bg-gray-800 text-white p-4 flex justify-between items-center">
    <h1 class="text-2xl font-bold">Diabgeet</h1>
    <nav>
      <ul class="flex space">
        <li class="mr-4"><a href="#" class="text-white hover:text-gray-400">Home</a></li>
        <li class="mr-4"><a href="#" class="text-white hover:text-gray-400">About</a></li>
        <li class="mr-4"><a href="#" class="text-white hover:text-gray-400">Contact</a></li>
        <li><a href="#" class="text-white hover:text-gray-400">Login</a></li>
      </ul>
    </nav>
  </header>
</template>

// eslint-disable-next-line vue/block-lang
<script >
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
