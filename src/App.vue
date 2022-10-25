<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
// import HelloWorld from './components/HelloWorld.vue'
import { DynamicIslandPlayer } from 'js-dynamic-island-player'

</script>

<template>
  <div>
    <div id="iphone14pro">
      <div style="margin-top: 25px">
        <DynamicIslandPlayer/>
      </div>
    </div>
  </div>
</template>
<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
.container {
  display: flex;
  width: 300px;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}
.icon-container {
  margin: 20px 12px;
  width: 60px;
  height: 60px;
  border-radius: 20%;
  background-color: #ececec;
  position: relative;
}
.text-container {
  color: white;
  text-align: center;
  margin: 0;
  padding: 0;
  font-weight: 300;
}
#iphone14pro {
  position: relative;
  margin: auto;
  width: 395px;
  height: 344px;
  overflow: hidden;
  background-image: url(https://www.apple.com.cn/v/iphone-14-pro/a/images/overview/dynamic-island/dynamic_hw__btl4fomgspyu_large.png);
  background-size: 100% 100%;
  display: flex;
  justify-content: center;
}
</style>
