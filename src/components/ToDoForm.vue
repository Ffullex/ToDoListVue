<template>
<div id="area">
  <input type="text" value="Введите текст">
</div>
</template>

<script>
export default {
  name: "ToDoForm",
}
</script>

<style scoped>
#area{
  min-width: 500px;
  color: #6a0554;
  background-color: #b125cb;
}
#area input{
  color: aqua;
  background-color: #6a0554;
}
</style>