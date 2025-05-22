<template>
  <div>
  <HeaderApp v-if="showHeader"/>
    <h1 class="text-2xl font-bold text-center mt-4">Hello {{ name }}</h1>
    <button @click="showHeader = !showHeader" class="bg-blue-500 text-white px-4 py-2 rounded mt-4">
      Toggle Header
    </button>
  </div>
</template>

<!-- eslint-disable vue/block-lang -->
<script>
import HeaderApp from './components/HeaderApp.vue';


export default {
  name: 'App',
  components: {
    HeaderApp,
  },
  data() {
    return {
      name: 'Diabgeet',
      showHeader: true,
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
