<template>
  <a href="#" class="aqua" style="margin: 0 auto 100px">
    <span class="aqua-text">HOME</span>
    <span class="aqua-highlight"></span>
  </a>
</template>

<script>
export default {
  name: 'aqua',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.aqua {
  display: inline-block;
  width: 80px;
  height: 80px;
  position: relative;
  border: 1px solid rgba(0,0,0,0.5);
  border-radius: 50%;
  background: radial-gradient(circle farthest-side at bottom, #00D1F2 30%, #0055C1 80%);
  box-shadow: 0 2px 6px rgba(0,0,0,0.5), 0 2px 10px rgba(0,100,255, 0.7), 0 2px 6px rgba(0,0,0,0.5), 0 2px 10px rgba(0,100,255, 0.7), inset 0 0 10px rgba(0,0,150,0.6);

}
.aqua-text {
  display: inline-block;
  line-height: 80px;
	color: rgba(255, 255, 255, 0.9);
	font-size: 12pt;
	text-shadow: 0px 0px 2px rgba(0, 0, 0, 0.5), 0px 0px 4px rgba(255, 255, 255, 1);
	position: absolute;
	text-align: center;
	top: 0;
  left: 50%;
  transform: translateX(-50%);
	width: 100px;
	height: 100px;
	z-index: 1;
}
.aqua-highlight {
  position: absolute;
	border-radius: 100px;
	width: 100%;
	height: 100%;
	background-image: linear-gradient(top, rgba(250, 250, 255, 1) 0%, rgba(250, 250, 255, 0.7) 10%, rgba(250, 250, 255, 0) 100%);
	z-index: 3;
	top: -20%;
  left: 0;
	-webkit-transform: scale(0.8, 0.6);
}
</style>
