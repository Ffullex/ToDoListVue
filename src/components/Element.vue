<template>
  <div>
    <input type="checkbox"/>
    <span>{{element.id + '.'}}{{element.title + '    '}}</span>
    <button v-on:click="clear(element.id)">Удалить</button>
  </div>
</template>

<script>
import clear from './ToDoForm'
export default {
  name: "Element",
  props: {
    clear: [clear],
    element: Object,
  },

}

</script>

<style scoped>

</style>