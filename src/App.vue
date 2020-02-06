<template>
  <div id="app">
    <div v-if="waiting" class="waiting">
    </div>
    <div v-if="!firstFinished" class="video">
      <video src="./assets/theme.mp4" style="width: 100%; height: 100%" id="vdo" muted></video>
      <tips :state="state" @Step01_finished="handleFinished">
      </tips>
      <newtips :state02="state02" @Step02_finished="handleEnd">
      </newtips>
    </div>
    <transition name="fade">
    <div v-if="firstFinished">
      <Rheader @transfer="handleTransfer" class="no-select"></Rheader>
      <div class="trans">
        <transfer ref="trans" @name="handleProduct"></transfer>
      </div>
      <Float @transfer="handleTransfer"></Float>
      <router-view @transfer="handleTransfer"></router-view>
      <Form :Supername="name"></Form>
      <div class="bottom">
        <div class="firstline">
            <div class="Unit"><h1>
              没有动机，<br>
              就没有杀机。<br>
              <span style="font-family: Me; font-size: 1.5rem">
                No Intention,
              </span><br>
              <span style="font-family: Me; font-size: 1.5rem" class="alitteTop"><br>No Destruction.</span>
            </h1>
            </div>
            <div class="Unit"><img src="./assets/reverseLogo.png" alt=""></div>
            <div class="Unit red">
              <h1>你的一次转发，<br>
              可能使一头犀牛免于残杀。<br>
              <span style="font-family: Me; font-size: 1.2rem">
                Your forwarding may save a rhino from killing.
              </span>
              </h1>
            </div>
        </div>
        <div style="text-align: center;">
          <img src="./assets/DZI.png" alt="" style="height: 3.5rem">
        </div>
        <p class="copyright">
          <span style="font-family: FangZheng8bit">
          同济大学设计创意学院 2015级工业设计系 出品<br>
            College of Design and Innovation,Tongji University / Industry Design 2015
          </span>
        </p>
      </div>
    </div>

    </transition>

  </div>
</template>

<script>
  import 'font-awesome/css/font-awesome.min.css'
  import $ from 'jquery/dist/jquery.min'
  import Rheader from "./components/Rheader.vue"
  import Float from "./components/floatWindow.vue"
  import tips from "./components/smallTips.vue"
  import newtips from "./components/newTips.vue"
  import transfer from './components/transfer.vue'
  import Form from './components/Product.vue'
export default {
  name: 'App',
  data(){
    return {
      firstFinished: false,
      state: true,
      state02: true,
      joint: "1",
      waiting: true,
      name:""
    }
  },
  components:{
    tips,
    Float,
    Rheader,
    newtips,
    transfer,
    Form
  },
  methods:{
    handleFinished(){
      var video = document.getElementById('vdo');
      video.play()
    },
    handleEnd(){
      var video = document.getElementById('vdo');
      this.firstFinished = true
    },
    handleTransfer(){
      $(".trans").toggle();
    },
    handleProduct(payload){
      this.name = payload.name;
    }
  },
  mounted(){
    var video = document.getElementById('vdo');
    var flag01 = false;
    var flag02 = false;
    var that = this;


    video.ondurationchange = function () {
        video.oncanplaythrough=function () {
          that.waiting = false;
          video.play();
          video.ontimeupdate = function () {
          if (video.currentTime >= 6.5 && video.currentTime <= 7.5 && flag01 === false) {
            flag01 = true;
            video.pause();
            that.state = false
          }
          if (video.currentTime >= 18.5 && video.currentTime <= 19.5 && flag02 === false) {
            flag02 = true;
            video.pause();
            that.state02 = false
          }
          if (video.currentTime >= 22) {
            video.pause();
            that.firstFinished = true
          }
        }
      }
    }
  }
}
</script>

<style>
  .no-select{
    user-select: none;
  }
  @keyframes fade {
    0% {
      opacity: 1;
    }
    50%{
      opacity: 0.4;

    }
    100%{
      opacity:1;

    }
  }
  @keyframes bounce {
    0% {
      position: relative;
      top: -1rem;
      transform: rotateY(0deg);
    }
    50%{
      position: relative;
      top: 1rem;
      transform: rotateY(90deg);

    }
    100%{
      position: relative;
      top: -1rem;
      transform: rotateY(0deg);

    }
  }
  .fade-enter-active, .fade-leave-active {
    transition: opacity .5s;
  }
  .fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
    opacity: 0;
  }
  @font-face {
    font-family: "FangZheng8bit";
    src: url('./assets/sfont.svg') format('svg'),
    url('./assets/sfont.ttf') format('ttf'),
    url('./assets/sfont.woff') format('woff'),
    url('./assets/sfont.woff2') format('woff2'),
    url('./assets/sfont.eot') format('eot');
  }
  @font-face {
    font-family: "PingFang SC";
    src: url('./assets/PingFangBold.svg') format('svg'),
    url('./assets/PingFangBold.ttf') format('ttf'),
    url('./assets/PingFangBold.woff') format('woff'),
    url('./assets/PingFangBold.woff2') format('woff2'),
    url('./assets/PingFangBold.eot') format('eot');
  }
  @font-face {
    font-family: "Me";
    src: url('./assets/Me.svg') format('svg'),
    url('./assets/Me.ttf') format('ttf'),
    url('./assets/Me.woff') format('woff'),
    url('./assets/Me.woff2') format('woff2'),
    url('./assets/Me.eot') format('eot');
  }
body{
  margin: 0;
}
#app {
  transition: 0.3s;
  padding: 0;
  margin: 0;
  /*font-family: 'Avenir', Helvetica, Arial, sans-serif;*/
  /*-webkit-font-smoothing: antialiased;*/
  /*-moz-osx-font-smoothing: grayscale;*/
  /*text-align: center;*/
  /*color: #2c3e50;*/
  /*margin-top: 60px;*/
}
  .video{
    user-select: none;
    -moz-user-select: none;
    -webkit-user-select: none;
    -ms-user-select: none;
    height: 100vh;
    background-color: black;
  }
  .waiting{
    position: fixed;
    top: 0;
    height: 100vh;
    background-color: rgb(0, 0, 0);
    z-index: 9999;
    width: 100%;
    text-align: center;
    color: red;
    letter-spacing: 3rem;
    font-size: 2.5rem;
    font-family: FangZheng8bit;
  }
  .waiting h1{
    animation: fade 2s linear infinite;
    padding-top: 10rem;
  }
  .bonce{
    padding-top: 2rem;
    position: relative;
    top: 0;
    animation: bounce 1.2s linear infinite;
  }
  div.bottom{
    height: 27rem;
    background-color: black;
    margin-top: 4rem;
    padding-top: 4rem;
  }
  div.firstline{
    font-family: "PingFang SC";
    padding: 0 5%;
    /*padding-left: 15rem;*/
    display: flex;
    flex-direction: row;
    justify-content: space-around;
  }
  div.Unit img{
    width: 15rem;
  }
  div.Unit h1:nth-of-type(1){
    color: white;
  }
  div.Unit.red h1{
    padding-top: 1rem;
    color: red;
    font-size: 1.6rem;
  }
  div.Unit{
    /*width: 20rem;*/
    width: 30%;
  }
  div.Unit:nth-of-type(1){
    padding-left: 5rem;
    box-sizing: border-box;
  }
  div.Unit:nth-of-type(2){
    text-align: center;
    /*width: 30rem;*/
  }
  p.copyright{
    /*padding-right: 4rem;*/
    /*margin-top: 4rem;*/
    color: white;
    text-align: center;
    position: relative;
    bottom: -2.6rem;
    font-size: 1rem;
    font-family: "PingFang SC","Microsoft JhengHei UI";
  }
  span.alitteTop{
    display: inline-block;
    position: relative;
    top: -2rem;
  }
  .trans{
    display: none;
    /*opacity: 0;*/
  }
  @keyframes move {
    from{
      opacity: 0;
    }
    to{
      opacity: 1;
    }
  }
  .moveani{
    animation: move 1s linear;
    animation-fill-mode: forwards;
  }
</style>
