
<template>
  <div id="app">
    <TodoCard ></TodoCard>
    

  </div>
</template>

<script>
import TodoCard from './components/TodoCard'

export default {
  name: 'app',
  components: {
    TodoCard
  }
}
</script>

<style>

body {
  background-color: yellow;
}
</style>