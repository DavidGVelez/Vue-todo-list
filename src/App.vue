<template>
     <main class="container-wide">
          <Todo></Todo>
      </main>
</template>

<script>

import Todo from "./components/organisms/Todo"

export default {
  name: 'App',
  components: {
    Todo,

  }
}
</script>

<style lang="scss">

  .container-wide{

    display: flex;
    height: 100vh;
    background-color: gray;
  }
</style>


