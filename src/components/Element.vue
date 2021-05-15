<template>
  <div>
    <input type="checkbox"/>
    <span>{{element.id + '.'}}{{element.title + '    '}}</span>
    <button v-on:click="clear(element.id)">Удалить</button>
  </div>
</template>

<script>
export default {
  name: "Element",
  props: {
    clear: Function,
    element: Object,
  },

}

</script>

<style scoped>

</style>