<template>
  <div class="outer">
    <div class="block">
      <div class="inner">
        <Header/>
        <hr/>
        <ToDo />
        <hr/>
        <Like />
        <hr/>
        <reverse-counting />
        <hr/>
        <reverse-line />
        <hr/>
        <alert />
        <hr />
        <input v-model="inputCountTerm" type="number" />
        <Termometr :count-term="inputCountTerm" />
        <hr />
        <TrafficLight />
        <hr />
        <counter />
        <hr />
        <variable-step-counter />
        <hr />
        <select-box />
        <hr />
        <unimportant-information-component />
        <hr />
        <accessing-the-network />
      </div>
    </div>
  </div>
</template>

<script>
import ToDo from './components/ToDo';
import Header from "./components/Header";
import Like from "./components/Like";
import ReverseCounting from "./components/ReverseCounting";
import ReverseLine from "./components/ReverseLine";
import Alert from "./components/Alert";
import Termometr from "./components/Termometr"
import TrafficLight from "./components/TrafficLight";
import Counter from "./components/Counter";
import VariableStepCounter from "./components/VariableStepCounter";
import SelectBox from "./components/SelectBox";
import UnimportantInformationComponent from "./components/UnimportantInformationComponent";
import AccessingTheNetwork from "./components/AccessingTheNetwork";
export default {
  name: 'App',
  components: {
    AccessingTheNetwork,
    UnimportantInformationComponent,
    SelectBox,
    VariableStepCounter,
    Counter,
    TrafficLight,
    Termometr,
    Alert,
    ReverseLine,
    ReverseCounting,
    ToDo,
    Header,
    Like
  },
  data: () => ({
    inputCountTerm: 1,
  })
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000000;
}
body {
  height: 100%;
  padding: 0;
  background-color: aliceblue;
}
.outer {
  background-size: cover;
  height: 100%;
  box-sizing: border-box;
  display: flex;
  background-color: aliceblue;
  align-items: center;
 }
.block {
  display: block;
  text-align: start;
  background-color: aliceblue;
  box-shadow: 0 0 10px rgba(0,0,0,0.5);
  margin: 5% 0 0 30%;
  height: 100%;
  border-radius: 5%;
}

.inner {
  height: 100%;
  display: block;
  margin: 20px 20px 20px 20px;
}
</style>
