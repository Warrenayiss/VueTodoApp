<template>
  <h3>Todo App</h3>
  <form @submit.prevent="addNewTodo">
    <label for="newTodo">New Todo</label>
    <input>
    <button>Add new Todo</button>
  </form>
</template>

<script>

export default {
  setup() {
    function addNewTodo(){
      console.log("form submitted");
    }

    return {
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
