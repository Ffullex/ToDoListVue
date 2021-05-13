<template>
  <Header/>
  <ToDoForm />
</template>

<script>
import ToDoForm from './components/ToDoForm'
import Header from "./components/Header";
export default {
  name: 'App',
  components: {
    ToDoForm,
    Header
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
