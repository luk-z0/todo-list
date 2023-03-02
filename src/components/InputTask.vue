<template>
  <div class="search-input">
    <input class="new-todo" @keyup.enter="addTask" placeholder="O que precisa ser feito?">
  </div>
</template>

<script>
import { Task } from '../models/Task';

export default {
  data() {
    return {

    }
  },
  methods: {

    addTask($event) {
      let task = new Task()
      let value = $event.target.value
      task.completed = false
      task.title = value
      this.$emit('newTask',task,)
      $event.target.value = ''
    }
  }
}
</script>

<style>
.search-input {
  margin: 4%;
}

.new-todo {
  display: block;
  margin: 0 auto;
  border-radius: 5px;
  padding: 1%;
  width: 50%;
  text-align: center;
}
</style>
