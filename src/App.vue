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
      imgAlt: 'Logos',
      todos: [
  {
    "userId": 1,
    "id": 1,
    "title": "delectus aut autem",
    "completed": false
          },
          {
            "userId": 1,
            "id": 2,
            "title": "quis ut nam facilis et officia qui",
            imgSrc: 'https://cdn.discordapp.com/attachments/1131950982032050226/1159996586489828352/diabgeet.png',
            "completed": false
          },
          {
            "userId": 1,
            "id": 3,
            "title": "fugiat veniam minus",
            "completed": false
          },
          {
            "userId": 1,
            "id": 4,
            "title": "et porro tempora",
            "completed": true
          },
          {
            "userId": 1,
            "id": 5,
            "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
            "completed": false
          }
    ]
    }

  },
}
</script>

<template>
  <HeaderApp v-if="showHeader" />

  <img
  :src="imgSrc"
  :alt="imgAlt"
  />
    <div v-for="local in todos"
    v-bind:key="local.id"
    class="bg-gray-100 p-4 rounded-lg shadow-md mb-4"
    >
      <img
        v-if="local.imgSrc"
        :src="local.imgSrc"
        :alt="imgAlt"
        class="w-16 h-16 mb-2 rounded-full"
      />
      <h2 class="text-xl font-semibold mb-2">{{ local.title }}</h2>
      <p class="text-gray-600 mb-2">User ID: {{ local.userId }}</p>
      <p class="text-gray-600 mb-2">ID: {{ local.id }}</p>
      <p class="text-gray-600 mb-2">Completed: </p>
      <p v-if="local.completed" class="text-green-500">Yes</p>
      <p v-else class="text-red-500">No</p>
      <p>{{ local.completed }}</p>
    </div>
</template>

<style scoped>
</style>
