<template>
  <div>
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
  methods:{

    addTask($event){
      let task = new Task()
      let value = $event.target.value
      task.completed = false
      task.title = value
      console.log(task)
    }
  }
}
</script>

<style>

.new-todo{
  border-radius: 5px;
  padding: 1%;
  margin: 2%;
  width: 30%;
  margin-inline-start: 35%;
  text-align: center;
}

</style>
