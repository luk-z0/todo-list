<template>
  <section class="todoapp">
    <header class="header">
      <h1 class="todo-title">Tarefas</h1>
      <input-task></input-task>
    </header>
  </section>
</template>

<script>
import InputTask from './components/InputTask.vue'

export default {
  name: 'App',
  components: {
    InputTask
  }
}
</script>

<style>
* {
  padding: 0%;
  margin: 0%;
}

.todoapp {
  background-color: #1f6afc;
  margin: 5%;
  height: 70%;
}

.todo-title {
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  text-align: center;
  color: black;
  font-weight: bold;
}

</style>
