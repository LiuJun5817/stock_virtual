<template>
  <Nav/>
  <div id="main_container">
    <FlowChart class="left_box"/>
    <CoreContent class="CoreContent_box"/>
    <info class="right_box"></info>
  </div>
  
</template>

<script>
import Nav from './components/Nav.vue'
import FlowChart from './components/FlowChart.vue'
import CoreContent from './components/CoreContent.vue'
import Info from './components/Info.vue'

export default {
  name: 'App',
  components: {
    Nav,
    FlowChart,
    CoreContent,
    Info
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  /* margin-top: 60px; */
}
#main_container{
  width: 1520px;
}
.left_box{
  float: left;
}
.CoreContent_box{
  float: left;
  margin-left: 50px;
}
.right_box{
  float:right;
}
</style>
