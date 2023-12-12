<!-- App.vue -->
<template>
  <div id="app">
    <DynamicForm />
  </div>
</template>

<script>
import DynamicForm from './components/DynamicForm.vue'

export default {
  name: 'App',
  components: {
    DynamicForm
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
