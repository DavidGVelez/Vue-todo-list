<template>
      <div class="container-wide">
        <!-- <Form></Form>
        <List></List>     -->
        <TodoHeader></TodoHeader>
        <TodoBody></TodoBody>
      </div>
</template>

<script>
// import Form from "./components/Form"
// import List from "./components/List"
import TodoHeader from "./components/molecules/TodoHeader";
import TodoBody from "./components/molecules/TodoBody"
export default {
  name: 'App',
  components: {
    // Form,
    // List,
    TodoHeader,
    TodoBody
  }
}
</script>

<style lang="scss">

  .container-wide{
    max-width: 500px;
    margin: 5rem auto;
    display: flex;
    flex-wrap: wrap;
    // flex-direction: column;
   
  }
</style>
