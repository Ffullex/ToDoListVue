<template>
  <div class="clockface">{{num}} </div>
</template>

<script>
export default {
  name: "ReverseCounting",
  data: () => ({
    num: 10,
    list: [],
  }),
  mounted() {
    let timerId =  setInterval(() => {this.num -= 1}, 1000)
    // остановить вывод через 5 секунд
    setTimeout(() => { clearInterval(timerId); }, 10000);
  }
}

</script>
<style>
  .clockface {
    font-size: 24px;
    color: black;
    margin: 10px;
  }

</style>