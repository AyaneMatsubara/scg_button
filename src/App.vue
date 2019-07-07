<template>
  <div id="app">
    <h1 class="title">Aqua Button Component</h1>
    <blue-button :msg="msg" :height="height" :width="width"/>
    <div class="input-box">
      <div class="input-item"><label for="msg">text</label><input v-model="msg" name="msg"></div>
      <div class="input-item"><label for="height">height</label><input v-model="height" name="height"></div>
      <div class="input-item"><label for="width">width</label><input v-model="width" name="width"></div>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import AquaButton from './components/aqua'
import RedButton from './components/red-button'
import BlueButton from './components/blue-button'

export default {
  name: 'App',
  data(){
    return {
      msg: 'Hello',
      height: 70,
      width: 270
    }
  },
  components: {
    BlueButton
  }
}
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translateX(-50%)translateY(-50%);
}
.input-box {
  display: flex;
  justify-content: center;
  width: 80vw;
  max-width: 600px;
  margin: 100px auto 50px;
  flex-wrap: wrap;
}
.input-box input {
  font-size: 20px;
  width: 100%;
}
.input-item {
  width: 30%;
  margin: auto;
  position: relative;
  min-width: 170px;
}
label {
  position: absolute;
  top: -30px;
  left: 0;
  font-size: 20px;
}
input {
  -moz-appearance: none;
  -webkit-appearance:none;
  text-align: center;
  font-size: 12px;
  background-color: transparent;
  border: none;
  border-radius: 0;
  border-bottom: #d0d0d0 1px solid;
  transition: all 0.2s;
}
input:focus {
  border-bottom: #016ECB 1px solid;
  outline: 0;
}
@media screen and (max-width: 767px){
  #app {
    position: relative;
    top: unset;
    left: unset;
    transform: unset;
    padding: 50px 0;
  }
  .input-box {
    max-width: 300px;
    margin: 50px auto;
  }
  .input-item {
    margin: 20px auto 40px;
  }
  label {
    top: -25px;
  }
}
</style>
