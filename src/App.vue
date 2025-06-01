

<template>
 <div class="text-zinc-950  grid h:48 grid-cols-2 place-content-stretch gap-4 ...">
        <div ><RouterLink to="/" class=" hover:text-gray-400">Home</RouterLink></div>
        <div ><RouterLink :to="rotaDinamica" class=" hover:text-gray-400">About</RouterLink></div>
        <div ><RouterLink to="/contact" class=" hover:text-gray-400">Contact</RouterLink></div>
        <div ><RouterLink to="/usuarios/10" class=" hover:text-gray-400">Usuario</RouterLink></div>

      <RouterView class="col-span-2 bg-gray-100 p-4 rounded-lg shadow-md" />
  </div>
</template>
<!-- eslint-disable vue/block-lang -->
<script>


export default {
  name: 'App',
  components: {
  },
  data() {
    return {
      rotaDinamica: '/about',
    }
  },
  methods: {
    onClose(){
      this.showAlert = false
      console.log("fechado aq")
    }
  },
  watch: {
  },
  computed: {
  },
  beforeCreate() {
  },
  created() {
  },
  beforeMount() {
  },
  mounted() {
  },
  beforeUnmount() {
  },
  unmounted() {
  },

}
</script>
<style scoped>



</style>
