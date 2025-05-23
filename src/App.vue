

<template>
  <HeaderApp v-if="showHeader" />
  <div>
    One Wat data binding <br>
    Two-way data binding<br>
    v-model -> formulários
  </div>

  <div class="text-gray hover:text-gray-400">
    <label >  Nome  </label>
      <input
      class="browser-default border-2 border-gray-300 rounded-lg p-2"
      type="text"
      v-model="name">
      <br>
    <p>{{ name }}</p>

  </div>
  <div class>
      <label >  Nome  </label>
        <input
        class="browser-default border-2 border-gray-300 rounded-lg p-2"
        type="text"
        v-model="name">
        <br>
      <p>{{ name }}</p>
  </div>

  <div>
    <label for="sport">Choose a sport:</label>
    <select v-model="sports" id="sport">
      <option value="">Escolha</option>
      <option value="soccer">Soccer</option>
      <option value="basketball">Basketball</option>
      <option value="tennis">Tennis</option>
      <option value="baseball">Baseball</option>
    </select>
    {{ sports.text }}
  </div>

  <div>

    <label> Cores</label>
    <input type="checkbox" value="azul" v-model="colors"> azul
     <input type="checkbox" value="amarelo" v-model="colors"> amarelo
    {{ colors }}
  </div>

</template>
<!-- eslint-disable vue/block-lang -->
<script>
import HeaderApp from './components/HeaderApp.vue'

export default {
  name: 'App',
  components: {
    HeaderApp,
  },
  data() {
    return {
      showHeader: true,
      name: 'Marcelo',
      var: 'text',
      sports: '',
      colors: [],
    }
  }
}
</script>
<style scoped>

.text{
  color: aliceblue;
}


</style>
