<template>
  <div>
    <button
      @click="onClick"
      class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
    >
      Enviar
    </button>
  </div>
  <div
    @mouseover="onMouseover"
    @mouseout="onMouseout"
    class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
  >
    Passa aqui
  </div>
  <div>
    <form action="https://google.com" @submit.once="onClick">
      <input @keyup="onKeyUp"
        type="text"
        name="name"
        id="name"
        class="bg-gray-200 border border-gray-300 rounded py-2 px-4 mb-4"
        placeholder="Nome">
      <button
        type="submit"
        class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
      >
        Enviar
      </button>
    </form>
  </div>
</template>

<!-- eslint-disable vue/block-lang -->
<script>
// import HeaderApp from './components/HeaderApp.vue'

export default {
  name: 'App',
  components: {
    // HeaderApp,
  },
  data() {
    return {
      showHeader: true,
    }
  },
  methods: {
    onClick($event) {
      console.log('click', $event)
      // $event.preventDefault();
      // alert('clicou');
      // this.showHeader = !this.showHeader;
    },
    onMouseover() {
      console.log('mouseover')
    },
    onMouseout() {
      console.log('mouseout')
    },
     onKeyUp($event) {
      console.log('keyup', $event)
    },
  },
}
</script>

<style scoped></style>
