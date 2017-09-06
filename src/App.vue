<template>
  <div id="app">
    <an-slider>
      <an-slider-item>
        <p class="con1">1</p>
      </an-slider-item>
      <an-slider-item>
        <p class="con2">2</p>
      </an-slider-item>
    </an-slider>
  </div>
</template>

<script>
import anSlider from './an-slider.vue'
import anSliderItem from './an-slider-item.vue'
export default {
  name: 'app',
  created(){
    
  },
  data () {
    return {
      msg: 'this is dev branch'
    }
  },
  components:{
    "an-slider": anSlider,
    "an-slider-item": anSliderItem
  }
}
</script>

<style>
*{
  margin: 0; padding: 0;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 750px;
  height: 450px;
  margin: 60px auto 0;
}
.con1{
  width: 100%;
  height: 100%;
  background-color: green;
}
.con2{
  width: 100%;
  height: 100%;
  background-color: red;
}
</style>
