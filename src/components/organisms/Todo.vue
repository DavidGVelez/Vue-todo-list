<template>
      <div class="todo">
        <TodoHeader></TodoHeader>
        <TodoBody></TodoBody>
      </div>
</template>

<script>

import TodoHeader from "../molecules/TodoHeader";
import TodoBody from "../molecules/TodoBody"
export default {
  name: 'App',
  components: {

    TodoHeader,
    TodoBody
  }
}
</script>

<style lang="scss">

    .todo{
        display: flex;
        margin: auto;
        flex-wrap: wrap;
    }
</style>
