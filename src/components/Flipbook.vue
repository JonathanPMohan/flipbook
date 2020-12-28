<template>
  <flipbook class="flipbook" :pages="pages" v-slot="flipbook">
    <!-- <img alt="previous" @click="flipbook.flipLeft" class="previous" src="@/assets/TestImages/previous.png">
    <img alt="next" @click="flipbook.flipRight" class="next" src="@/assets/TestImages/next.png"> -->
     <button class="previous_button" @click="flipbook.flipLeft"><span>Previous</span></button>
     <button class="next_button" @click="flipbook.flipRight"><span>Next</span></button>
  </flipbook>
</template>

<script>
import flipbook from 'flipbook-vue'

export default {
  components: {
    flipbook,
  },
      data() {
    return {
      pages: [
           null,
           require ('@/assets/TestImages/test_a.png'),
           require ('@/assets/TestImages/test_b.png'),
           require ('@/assets/TestImages/test_c.png'),
           require ('@/assets/TestImages/test_d.png'),
           require ('@/assets/TestImages/test_e.png'),
           ]
    }
  },
    }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.flipbook {
  width: 90vw;
  height: 90vh;
}

.previous_button{
  border-radius: 10px;
  border: none;
  color:#42b983;
  background: #000;
  text-align: center;
  font-size: 28px;
  padding: 15px;
  width: 200px;
  transition: all 0.5s;
  cursor: pointer;
  margin: 5px;
}

.previous_button span {
  cursor: pointer;
  display: inline-block;
  position: relative;
  transition: 0.5s;
}

.previous_button span:after {
  content: '\00ab';
  position: absolute;
  opacity: 0;
  top: 0;
  left: -40px;
  transition: 0.5s;
}

.previous_button:hover span {
  padding-left: 25px;
}

.previous_button:hover span:after {
  opacity: 1;
  left: 0;
}
.next_button{
  border-radius: 10px;
  border: none;
  color:#e20943;
  background: #000;
  text-align: center;
  font-size: 28px;
  padding: 15px;
  width: 200px;
  transition: all 0.5s;
  cursor: pointer;
  margin: 5px;
}

.next_button span {
  cursor: pointer;
  display: inline-block;
  position: relative;
  transition: 0.5s;
}

.next_button span:after {
  content: '\00bb';
  position: absolute;
  opacity: 0;
  top: 0;
  right: -20px;
  transition: 0.5s;
}

.next_button:hover span {
  padding-right: 25px;
}

.next_button:hover span:after {
  opacity: 1;
  right: 0;
}
</style>
