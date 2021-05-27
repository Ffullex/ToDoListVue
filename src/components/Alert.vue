<template>
  <div class="alertLine">
    <div class="innerInfo">
      Введите текст:
      <input class="inLine" v-model="alertText"/>
    </div>

    <div class="outerInfo">
      Введите задержку:
      <input class="inLine" v-model="alertTime"/>
      <button class="gamburger" @click="alertDone">Запусти</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Alert",
  data: () => ({
    alertText: '',
    alertTime: '',
  }),
  methods: {
    alertDone: function (){
      setTimeout(() => alert(this.alertText), this.alertTime*1000);
    }
  }
}
</script>

<style scoped>
.innerInfo {
  margin: 10px;
}
.outerInfo {
  margin: 10px;
}
.alertLine {
  color: black;
}
.gamburger {
  margin-left: 10px;
  color: black;
  background-color: #abb6bd;
  border: none;
  box-shadow: 0 0 10px rgba(0,0,0,0.5);
}
.inLine {
  background-color: aliceblue;
  color: #000000;
  border: none;
  box-shadow: 0 0 10px rgba(0,0,0,0.5);
}
</style>