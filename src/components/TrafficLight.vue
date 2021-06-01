<template>
  <div class="trafficLight">Светофор
    <div :class="propTopLight">.</div>
    <div :class="propMidLight">.</div>
    <div :class="propBotLight">.</div>
  </div>
</template>

<script>
export default {
  name: "TrafficLight",
  data: () => ({
    timeCounter: 1,
  }),
  computed: {
    propTopLight: function () {
      return (this.timeCounter === 2) ? 'trafficRed' : 'trafficOff';
    },
    propMidLight: function () {
      return (this.timeCounter === 3 || this.timeCounter === 1) ? 'trafficYellow' : 'trafficOff';
    },
    propBotLight: function () {
      return (this.timeCounter === 4) ? 'trafficGreen' : 'trafficOff';
    },
  },
  mounted() {
  setInterval(() => {
      return this.timeCounter < 4 ? this.timeCounter += 1 : this.timeCounter = 1
    }, 500)

  },
}
</script>

<style scoped>
.trafficLight {
  color: black;
}
.trafficRed {
  max-width: 25px;
  border-radius: 50%;
  background-color: red;
}
.trafficYellow {
  max-width: 25px;
  border-radius: 50%;
  background-color: yellow;
}
.trafficGreen {
  max-width: 25px;
  border-radius: 50%;
  background-color: green;
}
.trafficOff {
  max-width: 25px;
  border-radius: 50%;
  background-color: black;
}
</style>