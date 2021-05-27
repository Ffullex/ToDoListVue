<template>
  <div class="reverseLine">
    <input class="inLine" v-model="userLine"/>
    <button class="gamburger" @click="reverseString">Разверни</button>
    <reversed-line :line="reverseUserLine" />
  </div>
</template>

<script>
import ReversedLine from "./ReversedLine";
export default {
  name: "ReverseLine",
  components: {ReversedLine},
  data: () => ({
    userLine: '',
    reverseUserLine: '',
  }),
  methods: {
  reverseString: function () {
    this.reverseUserLine = this.userLine.split("").reverse().join("");
  },
  }
}
</script>

<style scoped>
.reverseLine {
  font-size: 24px;
  color: black;
  margin: 10px;
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