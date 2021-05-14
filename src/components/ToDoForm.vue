<template>
<div id="area">
  <p>Введите текст:
    <input type="text" v-model="userText"  placeholder="Сам такой">
    <button v-on:click="add" > Добавить </button>
    <button v-on:click="clearAll"> Удалить всё </button>
  </p>

  <div v-for="item in list" id="list" :key="item.id">
    {{item.id + '. '}}{{item.title}}
  </div>


</div>
</template>

<script>
export default {
  name: "ToDoForm",
  data: () => ({
    userText: '',
    list:[],
    id: 1,
    // checkbox: checked =
  }),
  methods: {
    add: function (){
      this.list
        .push({
          id: this.id,
          title: this.userText,
          // checkbox: this.checkbox
        });
        this.userText = '';
        this.id += 1;

    },
    clearAll: function () {
      this.list
          .splice({
            id: this.id,
            userText: this.userText
          })
        this.id = 1;
      },
    clear: function () {
      this.list
        .splice({

        })
    }
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