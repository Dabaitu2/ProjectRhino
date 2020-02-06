<template>
  <div class="hello">

    <div class="section section01">
        <el-carousel height="100vh" :interval="10000" :autoplay="false">
          <el-carousel-item>
            <div class="slide01 section">
              <div class="title">
                <h1 class="extra">没有动机，</h1>
                <h1 class="extra">就没有杀机。</h1>
                <h2 class="extra red">No Intention,</h2>
                <h2 class="extra red">No Destruction.</h2>
              </div>
              <img src="../assets/logo.png" alt="" style="" class="ajust ajustpic">
              <p class="intro ajust">你的每一次转发，<br>可能使一头犀牛免于残杀</p>
              <p class="intro ajust" style="font-family: Me; position: relative; top: -1.5rem">Your forwarding may save a rhino from killing.</p>
            </div>
          </el-carousel-item>
          <el-carousel-item>
            <img src="../assets/xixingji.jpg" alt="" style="height: 100%">
          </el-carousel-item>
          <el-carousel-item>
            <img src="../assets/mono.png" alt="" style="height: 100%">
          </el-carousel-item>
          <el-carousel-item>
            <img src="../assets/prop3.jpg" alt="" style="height: 100%">
          </el-carousel-item>
        </el-carousel>
    </div>
    <div class="section section02">
      <div class="bigHead">
          <h2 class="headinfo textshadow courier" style="font-family: 'Courier New'; font-weight: 600">The Rhino horn makes no sense parted from rhino.
            <span>The Rhino horn makes no sense parted from rhino.</span>
          </h2>
      </div>
      <div class="container">
        <div class="windowWrapper">
          <window_02>
            <span slot="desc">
            Rhino horn has no medicinal properties
            </span>
            <span slot="Endetail">
Rhino's horn is different from most grazing animals' horns. It is not bone but epidermis, the derivative of epithelial tissue which is mainly consist of Keratin. In other words, its composition is basically the same as that of human hair, nails, and animal scales, feathers, hooves, claws, and cubs. Rhino horn makes no sense parted from rhino. If you believe in its effectiveness, chewing your own nails will also have the same effect.
          </span>
          </window_02>
        </div>
        <div class="divide">
          <img src="../assets/MournRhino.png" alt="" class="divideImg layer01">
          <img src="../assets/line.png" alt="" class="divideImg layer02">
          <span class="shadowBox">
            <p class="figureTips">@The death of last male northern white rhino.</p>
          </span>
        </div>
        <div class="windowWrapper">
        <window_02>
          <span slot="desc">
            Blood collection has no value
          </span>
          <span slot="Endetail">
Because of people's fever persuit of their horns, over 3 rhinos are killed every day , while nearly 1,000 forest rangers have sacrificed in order to protect them. The savage criminals shoot rhinos and even people for profits without mercy and hesitation.The collection at the cost of destroying life should be rejected by us.          </span>
          <span slot="EnAuthor">
            —— MA Weidu
          </span>
        </window_02>
      </div>
        <div class="triangle">
          <img src="../assets/lotLine.png" alt="" class="line">
        </div>
      </div>
      <div class="section section03">
          <h1 class="red digital">收藏的目的是让文明延续，而不是去毁灭。</h1>
        <div class="secondTitle">
          <h1 class="digital top">收藏的目的是让文明延续，而不是去毁灭。</h1>
          <h1 class="digital top">收藏的目的是让文明延续，而不是去毁灭。</h1>
          <h1 class="digital top">收藏的目的是让文明延续，而不是去毁灭。</h1>

          <h1 class="top digital helpwords" style="color: red">The purpose of collection is to keep civilization alive, rather than to destroy.</h1>
          <h1 class="top digital helpwords">The purpose of collection is to keep civilization alive, rather than to destroy.</h1>
          <h1 class="top digital helpwords">The purpose of collection is to keep civilization alive, rather than to destroy.</h1>
        </div>
        <span class="blackline"></span>
        <span class="blackline"></span>
        <div class="container container_02">
              <div class="alertWrapper"><window_03></window_03></div>
              <div class="alertWrapper"><window_03></window_03></div>
              <div class="alertWrapper"><window_03></window_03></div>
              <div class="alertWrapper"><window_03></window_03></div>
              <div class="alertWrapper"><window_03></window_03></div>
              <div class="alertWrapper"><window_03></window_03></div>
              <div class="alertWrapper"><window_03></window_03></div>
              <div class="alertWrapper"><window_03></window_03></div>
          <div class="noticeWrapper">
            <window_04></window_04>
          </div>
          <div class="triangle section_2_triangle">
            <!--<img src="../assets/triangle.png" alt="" class="angle">-->
          </div>
        </div>
      </div>
      <!--<div class="divideBar">-->
      </div>
      <div class="section section04">
        <span class="blackline"></span>
        <span class="blackline"></span>
        <div class="headerPart">
          <h1 class="digital thirdHead">我需要你的帮助<br>
            <span class="spec">I need your HELP</span>
          </h1>
        </div>
        <div class="section3_body">
          <img src="../assets/AnotherRhino.png" alt="" style="width: 100%; position: absolute; top: 18rem">
          <window_05></window_05>
        </div>
      </div>
      <div class="section">
        <div class="first">
          <img src="../assets/noCopyrightLogo.png" alt="">
          <h1 class="digital">假如所有的动物都灭绝，下一个会是谁？</h1>
          <h1 class="courier">If all the animals were extinct, who would be the next?</h1>
        </div>
        <div class="second">
          <props @transfer="handleMiddleware">
            <span slot="info">
              FORWARDING
            </span>
            <span slot="btnInfo">&nbsp;立即转发</span></props>
          <props2>
            <span slot="info02">
              DONATION
            </span>
            <span slot="btnInfo02">&nbsp;立即捐赠</span></props2>
        </div>
        <p class="sorry">假如您浏览网站时感到不适，我们对此深感抱歉，这一切都是为了用另一种方式，来保护犀牛。<br>
         <span>If you feel uncomfortable while browsing the site, we are deeply sorry for it. All of this is to protect the rhino in another way.</span>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
  import $ from 'jquery/dist/jquery.min'
  import window_02 from './Section2window.vue'
  import window_03 from './section3window.vue'
  import window_04 from './Section4Window.vue'
  import window_05 from './section5window.vue'
  import props from './props.vue'
  import props2 from './props2.vue'



export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      castate: false,
      inter: 10000
    }
  },
  methods:{
    handleMiddleware(){
      this.$emit("transfer");
    },
  },

  components:{
    window_02,
    window_03,
    window_04,
    window_05,
    props,
    props2,
  },
  mounted(){
    this.castate = true;
    var Y = $(window).height();
    $(window).scroll(function(){
      var len = $(window).scrollTop()/Y;
//      console.log(len)
      if(len > 3.2 && len< 4.4) {
        if(!$(".alertWrapper").hasClass("bounce")) {
//          console.log("yes");
          $(".alertWrapper").addClass("bounce")
        }
      } else if(len>5 || len<2){
        $(".alertWrapper").removeClass("bounce")
      }
    })
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped type="text/scss">
  .digital{
    font-family: FangZheng8bit;
    font-weight: 400;

  }
  .courier{
    font-family: "Courier New";
  }
  .red{
    color: red;
  }
  .hello{
    width: 100%;
    overflow: hidden;
  }
  h1.thirdHead{
    background-color: black;
    height: 13rem;
    line-height: 5rem;
    color: white;
    font-size: 3rem;
    font-weight: 400;
    /*padding-left: 2rem;*/
    margin-bottom: 0;
    text-align: center;
    text-shadow: 2px -1px 0 red;
    letter-spacing: 4px;
    padding: 1rem;
    padding-top: 2rem;
  }
  @keyframes bounce {
    0% {
      top: -20px;
      opacity: 1;
    }
    50%{
      top: 0.6rem;
      opacity: 0.3;
    }
    100% {
      top: -20px;
      opacity:1;
    }
  }
  @keyframes fade {
    0% {
      color: black;
    }
    50%{
      color: red;
    }
    100%{
      color: black;
    }
  }
  div.container{
    padding: 2rem;
    text-align: center;
  }
  .bounce{
    animation: fallDown 1s linear;
    border-color: green;
  }
a {
  color: #42b983;
}
  div.section{
    position: relative;
    min-height: 100vh;
    /*background-color: #5daafa;*/
  }
  div.down{
    width: 100%;
    position: absolute;
    bottom: 3rem;
    text-align: center;
  }
  div.down img{
position: relative;
    width: 2.5rem;
    animation: bounce 3s linear infinite;
  }
  p{
    font-family: "FangZheng8bit";
  }
  p.intro{
    font-family: "PingFang SC","Microsoft JhengHei UI";
    padding-top: 10px;
    line-height: 1.4rem;
    /*animation: fade 1s linear infinite;*/
  }
  div.title{
    padding-top: 10rem;
    padding-left: 6.4rem;
  }
  h1.extra{
    font-family: "PingFang SC";
    font-weight: 800;
    font-size: 65px;
    line-height: 50px;
  }
  h2{
    margin-bottom: 0;
    padding-bottom: 0;
    font-family:"PingFang SC";
    font-size: 30px;
    line-height: 40px;
  }
  h2.extra:nth-of-type(1){
    margin-top: 4rem;
  }
  h2.extra:nth-of-type(2){
    margin-top: 5px;
  }
  div.bigHead{
    height: 17rem;
    background-color: black;
  }
  h2.headinfo{
    padding-top: 5rem;
    text-align: center;
    font-family: FangZheng8bit;
    color: #42b983;
    margin-top: 0;
    font-weight: normal;
    margin-bottom: 0;
  }
  h2.headinfo:nth-of-type(2){
    padding-top: 0rem;
    position: relative;
    top: -2rem;
  }
  h2.headinfo.textshadow span{
    display: block;
    position: relative;
    top: -41.5px;
    color: white;
  }
  div.windowWrapper{
    display: inline-block;
    text-align:center;
    height: 33rem;
    overflow: hidden;
    width: 55rem;
    position: relative;
  }
  .divideImg{
    /*position: relative;*/
    top: -5rem;
    width: 45rem;
  }
  img.layer02{
    position: absolute;
    z-index: 6;
    top: -0.5rem;
    left: 2rem;
  }
  img.layer01{
    top: -4rem;
    left: -2rem;
    position: absolute;
    z-index: 7;

  }
  span.shadowBox{
    display: inline-block;
    width: 54rem;
    height: 24rem;
    background-color: rgba(0, 214, 0, 0.8);
    position: absolute;
    z-index: 5;
    top: 2rem;
    left:-2rem;
    z-index: -1;

  }
  .divide{
    position: relative;
    height: 24rem;
  }
  div.triangle{
    top: -4rem;
    height: 1rem;
    position: relative;
  }
  img.angle{
    width: 5rem;
    position: absolute;
    left: 2rem;
  }
  h1.red.digital{
    margin-top: 2rem;
    padding-top: 1rem;
    padding-left: 2rem;
  }
  h1.top{
    padding-left: 2rem;
  }

  h1.top:nth-of-type(1){
    position: relative;
    top: -1rem;
    background-color: black;
    color: white;
  }

  h1.top:nth-of-type(2){
    position: relative;
    top: -3rem;
    /*background-color: black;*/
    color: white;
  }
  h1.top:nth-of-type(3){
    position: relative;
    top: -5rem;
    /*background-color: black;*/
    color: white;
  }
  .secondTitle{
    background-color: black;
    height: 7.2rem;
  }
  .alertWrapper{
    display: inline-block;
    position: absolute;
    top: 3rem;
    margin-left: 1rem;
    margin-bottom: 0.5rem;
    margin-top:0.5rem;
    opacity: 1;
  }
  .alertWrapper:nth-of-type(1){
    left: 4rem;
    z-index: 9;
    top: 20.5rem;

  }
  .alertWrapper:nth-of-type(2){
    left: 11rem;
    top: 18rem;

    z-index: 8;
  }
  .alertWrapper:nth-of-type(3){
    left: 18rem;
    z-index: 7;
    top: 15.5rem;

  }
  .alertWrapper:nth-of-type(4){
    left: 25rem;
    z-index: 6;
    top: 13rem;

  }
  .alertWrapper:nth-of-type(5){
    left: 32rem;
    z-index: 5;
    top: 10.5rem;

  }
  .alertWrapper:nth-of-type(6){
    left: 39rem;
    z-index: 4;
    top: 8rem;


  }
  .alertWrapper:nth-of-type(7){
    left: 46rem;
    z-index: 3;
    top: 5.5rem;


  }
  .alertWrapper:nth-of-type(8){
    left: 53rem;
    z-index: 2;

  }
  .noticeWrapper{
    top: 24rem;
    position: absolute;
    z-index: 10;
    left: calc(50% - 11rem);
  }
  .container_02{
    position: relative;
    z-index: 1;
    height: 65rem;
  }
  span.blackline{
    position: relative;
    top: -10px;
    display: inline-block;
    height: 3px;
    width: 100%;
    margin-top: 0px;
    background-color: black;
  }
  span.blackline:nth-of-type(2){
    top: -23px;
  }
  .section_2_triangle{
    position: absolute;
    top: 62rem !important;
    height: 5rem !important;
  }
  .section_2_triangle img.angle{
    margin-left: 70rem;
  }
  .section04{
    height: 70.65rem;
  }

  @keyframes fallDown {
    from{
      top: 0;
      opacity: 0;
    }
    to{
    }
  }
  p.figureTips{
    position: absolute;
    bottom: 4rem;
    padding-left: 1.5rem;
    font-family: Me, "PingFang SC", "Microsoft JhengHei UI";
  }
  p.figureTips:nth-of-type(2){
    position: absolute;
    bottom: 2.5rem;
    padding-left: 1.5rem;
  }
  .section03 h1{
    padding-left: 6.4rem !important;
  }
  img.line{
    height: 7rem;
    position: absolute;
    right: -2rem;
  }
  .section03{
    padding-top: 8rem;
  }
  h1.helpwords{
    position: relative;
    top: -5.2rem;
    font-size: 1rem;
    font-family: "Courier New";
    font-weight: 600;
    color: white;
  }
  #app > div > div.hello > div.section.section02 > div.section.section03 > div.secondTitle > h1:nth-child(5){
    position: relative;
    top: -6.4rem !important;
  }
  #app > div > div.hello > div.section.section02 > div.section.section03 > div.secondTitle > h1:nth-child(6){
    position: relative;
    top: -7.6rem !important;
  }
  .section04 span{
    top: 3rem;
  }
  .section04 span:nth-of-type(2){
    top: 2.05rem;
  }
  span.spec{
    font-family: "Courier New",Me, Consolas;
    font-size: 2rem;
    position: relative;
    top: -1rem;
    letter-spacing: 0;
  }
  #app > div > div.hello > div:nth-child(4){
    padding-top: 2rem;
  }
  div.first{
    text-align: center;
    padding: 1rem;
  }
  div.first img{
    width: 7rem;
    margin-bottom: 1rem;
  }
  div.first h1.courier{
    font-size: 1.5rem;
    color: #3c3c3c;
  }
  div.second{
    padding: 0 8rem;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
  }
  p.sorry{
    margin-top: 5rem;
    text-align: center;
    font-family: "PingFang SC","Microsoft JhengHei UI Light";
  }
  p.sorry span{
    font-family: Me;
  }
  h2.extra{
    padding-bottom: 1rem;
    font-size: 3rem;
  }
  .slide01{
    height: 100vh;
    background: url("../assets/bg.png") no-repeat right;
    background-size:82.2%;
  }
  .ajust{
    padding-left: 3.2rem;
  }
  .ajustpic{
    width: 5rem; margin-top: 5rem;
  }
  .el-carousel__item{
    height: 100vh;
  }
  .el-carousel__item h3 {
    color: #475669;
    font-size: 18px;
    opacity: 0.75;
    /*line-height: 100vh;*/
    margin: 0;
  }
  .el-carousel__item:nth-of-type(1) {
    background-color: #ffffff;
  }
  .el-carousel__item:nth-child(2n) {
    background-color: #ffffff;
  }

  .el-carousel__item:nth-child(2n+1) {
    background-color: #ffffff;
  }
  .title .extra.red{
    font-family: Me;
    font-size: 3.2rem
  }

  @media screen and (max-width: 1024px){
    .title .extra{
      font-size: 2rem;
    }
    .title .extra.red{
      font-size: 2rem;
    }
    div.title{
      /*padding: 0 !important;*/
      background-position: 0 0 !important;
      padding-top: 24rem;
      padding-left: 2rem;
    }
    div.slide01{
      padding-top: 0;
      background-size:100%;
      background-position: 0 4rem;

    }
    h1.extra{
      line-height: 15px;
    }
    h2.red.extra{
      margin-top: 0;
      line-height: 15px;
    }
    img.ajustpic{
      margin-top: 1rem;
      margin-left:0;
      margin: 0 auto;
      padding-left: calc(50% - 2.8rem);
    }
    p.intro.ajust{
      padding-left: 0 !important;
      text-align: center;
      font-size: 0.6rem;
      line-height: 1rem;
    }

  }

</style>
