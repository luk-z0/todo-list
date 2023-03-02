<template>
  <ul class="todo-list">
    <li v-for="todo in todoList" class="todo">
      <div class="view">
        <label>{{ todo.title }}</label>
      </div>
    </li>
  </ul>
</template>

<script>
export default {
  props: ['todoList'],
}
</script>

<style>


.todo {
  list-style: none;
}

.view {
  background-color: rgb(43, 89, 241);
  padding: 2%;
  margin: 1%;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  font-size: 20px;
  font-weight: bold;
  text-align: center;
  margin-inline-start: auto;
  margin-inline-end: auto;
  border-radius: 20px;
  box-shadow: 2px 5px 15px;
}
</style>
