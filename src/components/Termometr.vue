<template>
  <div :class=propsName > {{countTerm}}</div>
</template>

<script>
export default {
  name: "Termometr",
  props:{
    countTerm: Number,
  },
  computed: {
    propsName: function () {
        return (this.countTerm > 0) ? 'hotText' : 'coldText'
    }
  }
}
</script>

<style scoped>
.hotText {
  color: red;
}
.coldText {
  color: blue;
}
.countTerm {
  background-color: aliceblue;
  color: #000000;
  border: none;
  box-shadow: 0 0 10px rgba(0,0,0,0.5);
  margin: 10px;
}
</style>