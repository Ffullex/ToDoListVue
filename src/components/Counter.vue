<template>
<div>
  <button class="gamburger" @click="clicker">Нажми меня</button>
  <div class="counter">{{counter}}</div>
</div>
</template>

<script>
export default {
  name: "9Counter",
  data:() => ({
  counter: 0,
}),
  methods: {
    clicker: function (){
      this.counter = this.counter + 1;
    }
  }
}
</script>

<style scoped>
.gamburger {
  margin-left: 10px;
  color: black;
  background-color: #00ff04;
  border: none;
  box-shadow: 0 0 10px rgba(0,0,0,0.5);
}
.counter {
  background-color: aliceblue;
  color: #000000;
  border: none;
  box-shadow: 0 0 10px rgba(0,0,0,0.5);
  width: 30px;
  margin: 10px;
  border-radius: 5%;
}
</style>