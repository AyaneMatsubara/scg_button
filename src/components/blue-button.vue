<template>
  <div>
    <a href="#" class="blue" v-bind:style="{ height: inner_size(height)+'px', width: inner_size(width)+'px', borderRadius: border_radius(inner_size(height))+'px' }">
      <span class="blue-text" v-bind:style="{ lineHeight: inner_size(height)+'px' }">{{ msg }}</span>
      <span class="blue-highlight"></span>
      <div class="blue-frame" v-bind:style="{ height: height+'px', width: width+'px', borderRadius: border_radius(height)+'px' }"></div>
    </a>
  </div>
</template>

<script>
export default {
  name: 'blue-button',
  props: ['msg', 'height', 'width'],
  methods: {
    border_radius(size) { return size / 2 },
    inner_size(size) { return size - 20 }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.blue {
  display: inline-block;
  position: relative;
  margin: 10px;
  border: 1px solid rgba(0,0,0,0.5);
  background: radial-gradient(circle at bottom, #00D1F2 20%, #0055C1 85%);
  box-shadow: 0 2px 6px rgba(0,0,0,0.5), 0 2px 10px rgba(0,100,255, 0.7), 0 2px 6px rgba(0,0,0,0.5), 0 2px 10px rgba(0,100,255, 0.7), inset 0 0 10px rgba(0,0,150,0.6);
  font-size: 16px;
  transition: all 0.3s;
}
.blue:hover {
  box-shadow: 0 2px 6px rgba(0,0,0,0.3), 0 2px 10px rgba(0,100,255, 0.5), 0 2px 6px rgba(0,0,0,0.3), 0 2px 10px rgba(0,100,255, 0.5), inset 0 0 12px rgba(0,0,180,1);
}
.blue-text {
  display: inline-block;
  width: 75%;
  overflow: hidden;
	color: rgba(255, 255, 255, 0.9);
	text-shadow: 0px 0px 2px rgba(0, 0, 0, 0.5), 0px 0px 4px rgba(255, 255, 255, 1);
	position: absolute;
	text-align: center;
	top: 0;
  left: 50%;
  transform: translateX(-50%);
	z-index: 1;
}
.blue-highlight {
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
.blue-frame {
  margin: auto;
  position: absolute;
  top: -10px;
  left: -10px;
  background-image: linear-gradient(to top left, #F7DE05, #DA8E00, #EDAC06, #F7DE05, #ECB802, #DAAF08, #B67B03);
  z-index: -99;
  border: #A87400 solid 1px;
  box-shadow: #845305 0px 1px 7px;
}
</style>
