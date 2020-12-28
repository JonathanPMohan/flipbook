<template>
  <div id="app">
    <img alt="Punch-Out logo" class="punch_out_logo" src="./assets/punch_out_logo.png">
    <Flipbook />
  </div>
</template>

<script>
import Flipbook from './components/Flipbook.vue'

export default {
  name: 'App',
  components: {
    Flipbook
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #31e90c;
  margin-top: 60px;
  background: #000;
  background-image: url('~@/assets/punch_out_BKG.png');
}
.punch_out_logo {
  width: 75%;
}
</style>
