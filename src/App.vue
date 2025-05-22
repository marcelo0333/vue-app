<template>
  <div>
    {{ fullName }}
    <h2 class="bg-amber-950 p-1.5 ">Todos Incompletas</h2>
    <div v-for="todo in unCompleted" :key="todo.id" class="bg-gray-200 p-4 mb-2">
      {{ todo.title }} <span v-if="todo.completed">Completed</span>
    </div>
    <h2 class="bg-amber-950 p-1.5">Todos Completas</h2>
    <div v-for="todo in completed" :key="todo.id" class="bg-gray-200 p-4 mb-2">
      {{ todo.title }} <span v-if="todo.completed">Completed</span>
    </div>
    <br><br>
     <div v-for="todo in todos" :key="todo.id" class="bg-gray-200 p-4 mb-2">
      <input
      v-model="todo.completed"
      type="checkbox"
      class="mr-2">
    {{ todo.title }}
    </div>
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
      user: {
        name: 'John Doe',
        lastName: 'Doe',
      },
      todos:[
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
        ],

    }
  },
  computed: {
    fullName() {
      return `${this.user.name} ${this.user.lastName}`;
    },
    unCompleted(){
      return this.todos.filter(todo => todo.completed === false);
    },
     completed(){
      return this.todos.filter(todo => todo.completed === true);
    }
  },
  methods: {
  },
}
</script>

<style scoped>
</style>
