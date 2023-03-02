<template>
  <section class="todoapp">
    <header class="header">
      <h1 class="todo-title">Tarefas</h1>
    </header>
    <input-task @newTask="addTask"></input-task>
    <task-list :todo-list="tasks"></task-list>
  </section>
</template>

<script>
import InputTask from './components/InputTask.vue'
import TaskList from './components/TaskList.vue'
import { Task } from './models/Task'

let tasks = []
let task = new Task()


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
  },
  methods: {
    addTask(task){
      this.tasks.push(task)
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
  margin: 2%;
  padding: 5%;
  height: 480px;
  box-shadow: 10px 8px 20px;
  border-radius: 20px;
}

.todo-title {
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  text-align: center;
  color: black;
  font-weight: bold;
  font-size: xx-large;
}
</style>
