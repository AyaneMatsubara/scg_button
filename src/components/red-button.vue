<template>
  <div>
    <a href="#" class="red">
      <span class="red-text">{{ msg }}</span>
      <span class="red-highlight"></span>
    </a>
    <br>
    <br>
    <input v-model="msg" style="font-size:20px;">
  </div>
</template>

<script>
export default {
  name: 'red-button',
  data () {
    return {
      msg: 'START'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.red {
  display: inline-block;
  width: 250px;
  height: 50px;
  position: relative;
  border: 1px solid rgba(0,0,0,0.5);
  border-radius: 25px;
  background: radial-gradient(circle at bottom, #FE3101 20%, #620000 85%);
  box-shadow: 0 2px 6px rgba(0,0,0,0.5), 0 2px 10px rgba(255,100,0, 0.7), 0 2px 6px rgba(0,0,0,0.5), 0 2px 10px rgba(255,100,0, 0.7), inset 0 0 10px rgba(150,0,0,0.6);
}
.red-text {
  display: inline-block;
  line-height: 50px;
	color: rgba(255, 255, 255, 0.9);
	font-size: 12pt;
	text-shadow: 0px 0px 2px rgba(0, 0, 0, 0.5), 0px 0px 4px rgba(255, 255, 255, 1);
	position: absolute;
	text-align: center;
	top: 0;
  left: 50%;
  transform: translateX(-50%);
	height: 100px;
	z-index: 1;
}
.red-highlight {
  position: absolute;
	border-radius: 100px;
	width: 100%;
	height: 100%;
	background-image: linear-gradient(top, rgba(250, 250, 255, 0.6) 0%, rgba(250, 250, 255, 0.4) 10%, rgba(250, 250, 255, 0) 60%);
	z-index: 3;
	top: -20%;
  left: 0;
	-webkit-transform: scale(0.8, 0.6);
}
.red::after {
  position: absolute;
  top: -10px;
  left: -10px;
  content: "";
  width: 270px;
  height: 70px;
  width: 270px;
  height: 70px;
  /*background: #F3C857;*/
  background-image: linear-gradient(to top left, #F7DE05, #DA8E00, #EDAC06, #F7DE05, #ECB802, #DAAF08, #B67B03);
  z-index: -99;
  border-radius: 35px;
  border: #A87400 solid 1px;
  box-shadow: #845305 0px 1px 7px;
}

.btn {
  position: relative;
  display: inline-block;
  padding: 0.5em 0.75em;
  text-decoration: none;
  color: #FFF;
  background: #005EAC;
  background-image: -webkit-linear-gradient(transparent 0%,rgba(255,255,255,.3) 50%,transparent 50%,rgba(0,0,0,.1) 100%);
  background-image: linear-gradient(transparent 0%,rgba(255,255,255,.3) 50%,transparent 50%,rgba(0,0,0,.1) 100%);
  border-radius: 4px;
  box-shadow: inset 0 2px 0 rgba(255,255,255,0.2), inset 0 -2px 0 rgba(0, 0, 0, 0.05);
  font-size: 20px;
  font-weight: bold;
  /*font-family: 'Sawarabi Mincho', sans-serif;*/
}
.btn:active {
  box-shadow: 0 0 2px rgba(0, 0, 0, 0.30);
}
.btn::before {
  position: absolute;
  top: -8%;
  left: -3%;
  content: "";
  width: 106%;
  height: 116%;
  /*background: #F3C857;*/
  background-image: linear-gradient(to top left, #F7DE05, #DA8E00, #EDAC06, #F7DE05, #ECB802, #DAAF08, #B67B03);
  z-index: -99;
  border-radius: 4px;
}
</style>
