<template>
  <div>
      <div 
          v-for="(obj, index) in todos"
          v-bind:key="obj.id"
          class="todos-items"
      >
          {{ index }} - {{ obj.title }}
      </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      todos: [
        {
          "userId": 1,
          "id": 1,
          "title": "Estudar vue",
          "completed": false
        },
        {
          "userId": 1,
          "id": 1,
          "title": "Estudar react",
          "completed": false
        }
      ]
    }
  }
}
</script>

<style>
.todos-items {
  background: #000;
  margin: 0 0 5px 0;
  padding: 3px 5px;
  color: #fff;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
