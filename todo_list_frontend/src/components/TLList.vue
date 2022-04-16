<template>
  <ul class="todo-main">
    <TLItem v-for="todo in todos" :key="todo.id" :todo="todo"
            :checkTodo="checkTodo" :deleteTodo="deleteTodo"></TLItem>
  </ul>
</template>

<script>
import TLItem from "@/components/TLItem";

export default {
  name: 'TLList',
  components: {
    TLItem,
  },
  props: ['todos', 'checkTodo', 'deleteTodo']
}
</script>

<style scoped>
/*main*/
.todo-main {
  margin-left: 0px;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0px;
}
.todo-empty {
  height: 40px;
  line-height: 40px;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding-left: 5px;
  margin-top: 10px;
}
</style>
