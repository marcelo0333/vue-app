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
  computed: {
  },
  watch: {
  },
  methods: {
  },
  // Criação
    //Preparar o Componente
    //Ajax, Inicializar variaveis
    //Sem acesso ao DOM
  // Montagem
    //Inicializar Lib Externa (new Lib())
    //Precisa de acesso ao DOM
    //Tem acesso ao DOM
  //Atualização
    //Debug
    //Update
  //Desmontagem
    //Remover tudo aquilo que for necessario (lib->destroy)
    //Para assim liberar memória.

  //Hooks

  // beforeCreate() {
  //   console.log('beforeCreate');
  //     console.log("Estado:", this.name);
  //     console.log("DOM", this.$el);
  //   // Aqui podemos inicializar uma lib externa
  // },
  // created() {
  //   console.log('created');
  //       console.log("Estado:", this.name);
  //             console.log("DOM", this.$el);

  //   // this.$emit('update:show', false);
  // },
  // beforeMount() {
  //   console.log('beforeMount');
  //       console.log("Estado:", this.name);
  //             console.log("DOM", this.$el);

  //   // Aqui podemos inicializar uma lib externa
  // },

}
</script>

<style scoped>
</style>
