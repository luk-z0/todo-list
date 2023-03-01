<template>
  <section class="todoapp">
    <header class="header">
      <h1 class="todo-title">Tarefas</h1>
    </header>
    <input-task></input-task>
    <task-list :todo-list="tasks"></task-list>
  </section>
</template>

<script>
import InputTask from './components/InputTask.vue'
import TaskList from './components/TaskList.vue'
import { Task } from './models/Task'

let tasks = []
let task = new Task()
task.completed = false
task.title = 'Tarefa'
tasks.push(task)
tasks.push(task)
tasks.push(task)

export default {
  name: 'App',
  components: {
    InputTask,
    TaskList
  },
  data() {
    return {
      tasks: tasks
    }
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
