<template>
  <div id="app">
    <!--<img src="./assets/logo.png">
    <HelloWorld/>-->
    <aqua-button/>
    <br>
    <red-button/>
    <br>
    <br>
    <blue-button v-bind:height="50" v-bind:width="250" v-bind:text="'START'" class="margin"/>
    <br>
    <br>
    <blue-button v-bind:height="40" v-bind:width="150" v-bind:text="'hello'"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import AquaButton from './components/aqua'
import RedButton from './components/red-button'
import BlueButton from './components/blue-button'

export default {
  name: 'App',
  components: {
    HelloWorld,
    RedButton,
    AquaButton,
    BlueButton
  }
}
</script>

<style>
.margin {
  margin: 50px;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
