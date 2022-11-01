<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
// import HelloWorld from './components/HelloWorld.vue'
import { DynamicIslandPlayer } from 'vue-dynamic-island-player'
import { ref } from 'vue'
import song1 from '@/assets/audio/rave_digger.mp3'
import song2 from '@/assets/audio/80s_vibe.mp3'
import cover1 from '@/assets/cover1.png'
import cover2 from '@/assets/cover2.png'
const player = ref()
const theme = ref()
const playList = ref([
  {
    title: 'Rave Digger',
    file: song1,
    howl: null,
    author: 'Cherrystones',
    cover: cover1
  },
  {
    title: '80s Vibe',
    file: song2,
    howl: null,
    author: 'Tory Lanez',
    cover: cover2
  }
])
function test () {
  console.log('233223')
}
function play () {
  console.log('play')
}
function next () {
  console.log('next')
}
function previous () {
  console.log('previous')
}
function pause () {
  console.log('pause')
}
function set () {
  player.value.setVolume(0.9)
}
function setMute () {
  player.value.setMute(true)
}
function setSound () {
  player.value.setMute(false)
}
function seekTo () {
  player.value.seekBySeconds(30)
}
function toggle () {
  player.value.toggle()
}
function playNext () {
  player.value.playNext()
}
function playPrevious () {
  player.value.playPrevious()
}
function getState () {
  console.log(player.value.getSoundState())
}
function setTheme (color) {
  theme.value = color
}
function setRate (val) {
  player.value.setRate(val)
}
</script>

<template>
  <div>
    <div id="iphone14pro">
      <div style="margin: 25px auto;">
        <DynamicIslandPlayer
            ref="player"
            :play-list="playList"
            :volume="0.8"
            :html5="true"
            :theme="theme"
            @play="play"
            @next="next"
            @pause="pause"
            @previous="previous"
            @animation-small="test" />

      </div>
    </div>
    <div class="control-area">
      <button @click="getState">get sound state</button>
      <button @click="set">set volume</button>
      <button @click="setMute">set mute</button>
      <button @click="setSound">set sound</button>
      <button @click="seekTo">jumpTo 30s</button>
      <button @click="toggle">play / pause</button>
      <button @click="playNext">next song</button>
      <button @click="playPrevious">previous song</button>
      <button @click="setRate(2.0)">set rate 2x</button>
      <button @click="setRate(1.0)">set rate 1x</button>
      <div style="display: flex;margin-top: 20px; align-items: center">
        <p>set theme:</p>
        <div class="theme-control">
          <button @click="setTheme('#272729')" style="background: #272729"></button>
          <button @click="setTheme('#e4393c')" style="background: #e4393c"></button>
          <button @click="setTheme('#747bff')" style="background: #747bff"></button>
        </div>

        <button @click="setTheme('https://m1.im5i.com/2022/10/31/UVQPwD.jpg')" style="">set picture</button>
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
  background-image: url(https://www.apple.com.cn/v/iphone-14-pro/a/images/overview/dynamic-island/dynamic_hw__btl4fomgspyu_large.png), url("./assets/bg.png");
  background-size: 100% 100%, 90% 100%;
  border-top-left-radius: 74px;
  border-top-right-radius: 74px;
  display: flex;
  justify-content: center;
  background-position-x: 0,17px;
  background-repeat: no-repeat;
}
.control-area {
  margin-top: 25px;
}
.control-area button {
  margin: 3px 16px;
}
.theme-control button {
  width: 30px;
  height: 30px;
  border-radius: 50%;
}
</style>
