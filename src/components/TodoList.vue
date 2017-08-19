<template>
<div>
  <!-- Javascript expressions in Vue are enclosed in double curly brackets.-->
  <p> Completed Tasks: {{todos.filter(todo => {return todo.done === true}).length}}</p>
  <p> Pending: {{todos.filter(todo => {return todo.done === false}).length}}</p>
  <!--we are passing the data to the todo component to render the todo list -->
  <todo v-for="todo in todos" v-bind:todo="todo"></todo>
</div>
</template>

<script type="text/javascript">
import Todo from './Todo'

export default {
  props: ['todos'],
  components: {
    Todo
  }
}
</script>

<style>
</style>
