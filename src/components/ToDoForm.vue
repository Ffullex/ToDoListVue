<template>
<div id="area">
  <p>Введите текст:
    <input type="text" v-model="userText"  placeholder="Сам такой">
    <button v-on:click="add" > Добавить </button>
    <button v-on:click="clearAll">Удалить</button>
  </p>

  <div v-for="item in list" id="list" :key="item.id">
      <Element :element="item" :clear="clear"/>
  </div>

</div>
</template>

<script>
import Element from "./Element";
export default {
  name: "ToDoForm",
  components: {
    Element
  },
  data: () => ({
    userText: '',
    list:[],
    id: 1,
  }),
  methods: {
    add: function (){
      this.list
        .push({
          id: this.id,
          title: this.userText,
        });
        this.userText = '';
        this.id += 1;
    },
    clearAll: function () {
      this.list = []
      this.id = 1;
    },
    clear: function (id) {this.list = this.list.filter(element => element.id !== id)
    this.id = id}
  }
}

</script>

<style scoped>
#area{
  min-width: 500px;
  color: #000000;
}
#area input{
  color: #000000;
}
#area button{
  color: #000000;
}
</style>