<template>
  <h3>Todo App</h3>
  <form @submit.prevent="addNewTodo">
    <label for="newTodo">New Todo</label>
    <input name="newTodo" v-model="newTodo">
    <button>Add new Todo</button>
  </form>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    //datas
    const newTodo = ref('')
    const todos = ref([])
    
    //functions
    function addNewTodo(){
      todos.value.push({
        done: false,
        content: newTodo.value
      })
      newTodo.value = ""
    }

    //returns
    return {
      newTodo,
      addNewTodo
    }
  }
}
</script>

<style>
body {
  font-family: sans-serif;
  padding-top: 1em;
  padding-bottom: 1em;
  font-size: 2em;
  width: 80%;
  margin: 0 auto;
}
input, textarea, button, p, div, section, article, select {
  display: 'block';
  width: 100%;
  font-family: sans-serif;
  font-size: 1em;
  margin: 0.5em;
}
.todo {
  cursor: pointer;
}
.done {
  text-decoration: line-through;
}
</style>
