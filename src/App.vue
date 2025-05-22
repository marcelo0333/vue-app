<template>
  <div>
    <h1 class="text-3xl font-bold underline p-0.5 mb-1.5">
      Formulario
    </h1>
    <input
    v-model="name"
    type="text"
    class="border border-gray-300 rounded p-2"
    >
    <br>
    {{ name }}

    <br><br><br>

    <select v-model="pageCount" class="border border-gray-300 rounded p-2">
      <option value="5">5</option>
      <option value="10">10</option>
      <option value="15">15</option>
    </select>
  </div>

      <br><br><br>
    <input
    v-model="user.firstName"
    type="text"
    class="border border-gray-300 rounded p-2"
    >
    <input
    v-model="user.lastName"
    type="text"
    class="border border-gray-300 rounded p-2"
    >
    <br>
    {{ firstName }}
    {{ lastName }}
    <br><br><br>

</template>

<!-- eslint-disable vue/block-lang -->
<script>
export default {
  name: 'App',
  components: {
  },
  data() {
    return {
      name: '',
      pageCount: 5,
      user: {
        firstName: '',
        lastName: ''
      },
    }
  },
  computed: {
  },
  watch: {
    name(vl) {
      if(vl.length > 3) {
              this.saveUser();
      }
    },
    pageCount(vl) {
      this.changePageCount(vl);
    },
    user: {
      handler(){
        console.log("mudou", this.user);
      },
      deep: true,
    }
  },
  methods: {
    saveUser() {
      console.log(this.name);

    },
    changePageCount(vl) {
      console.log("trocado", vl);
  },
}
}
</script>

<style scoped>
</style>
