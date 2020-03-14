<template>
  <div id="app" class="container">

    <h1 class="title has-text-centered">
      Final EEC <br>
      <!-- <span id="minutes">{{ minutes }}</span>
      <span id="middle">:</span>
      <span id="seconds">{{ seconds }}</span> -->
    </h1>

    <!-- <Timer date="03 April 2020 21:00"></Timer> -->

    <div class="buttons flex-center">
      <btn-pertanyaan nomor="1" pertanyaan="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Recusandae sed quo dicta odit. Ipsa, quisquam. Maiores, temporibus libero facere porro dolorum esse explicabo eum iusto amet quibusdam, facilis suscipit pariatur." :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="clickpertanyaan"></btn-pertanyaan>
      
      
      <btn-pertanyaan nomor="2" pertanyaan="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Recusandae sed quo dicta odit. Ipsa, quisquam. Maiores, temporibus libero facere porro dolorum esse explicabo eum iusto amet quibusdam, facilis suscipit pariatur." :timPenjawab="timpenjawab" :btnclass="timclass" :propclick="clickpertanyaan"></btn-pertanyaan>
      
    </div>
  </div>
</template>

<script>
import BtnPertanyaan from './components/ButtonPertanyaan.vue'
import Timer from './components/Timer'

export default {
  name: 'App',
  components: {
    BtnPertanyaan,
    Timer
  },
  data(){
    return{
      timpenjawab: null,
      timer: null,
      totalTime: 25 * 60,
      resetButton: false,
      timclass: 'button is-primary'
    }
  },
  methods: {
        clickpertanyaan: function(){
          if(this.timpenjawab === "Silver"){
            this.timclass = "button is-success"
          } else if(this.timpenjawab === "Flint"){
            this.timclass = "button is-success"
          }
        },
        startTimer: function() {
        this.timer = setInterval(() => this.countdown(), 1000);
        this.resetButton = true;
        this.title = "Greatness is within sight!!";
        },
        stopTimer: function() {
        clearInterval(this.timer);
        this.timer = null;
        this.resetButton = true;
        this.title = "Never quit, keep going!!";
        },
        resetTimer: function() {
        this.totalTime = 25 * 60;
        clearInterval(this.timer);
        this.timer = null;
        this.resetButton = false;
        this.title = "Let the countdown begin!!";
        },
        padTime: function(time) {
        return (time < 10 ? "0" : "") + time;
        },
        countdown: function() {
            if (this.totalTime >= 1) {
                this.totalTime--;
            } else {
                this.totalTime = 0;
                this.resetTimer();
            }
        }
    },
  // ========================
    computed: {
        minutes: function() {
        const minutes = Math.floor(this.totalTime / 60);
        return this.padTime(minutes);
        },
        seconds: function() {
        const seconds = this.totalTime - this.minutes * 60;
        return this.padTime(seconds);
        }
    }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
