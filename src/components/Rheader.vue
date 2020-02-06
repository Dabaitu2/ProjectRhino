<template>
  <div class="main">
    <div class="Rheader">
      <div class="left">
        <span class="line"></span>
        <span class="line"></span>
        <span class="line"></span>
      </div>
      <div class="center">
        <ul>
          <li @click="jumpto(1)">鉴定犀牛角</li>
          <li @click="jumpto(2)">购买渠道</li>
          <li @click="jumpto(3)">灭绝物语</li>
          <li @click="outWindow">转发行大运</li>
          <li @click="jumpto(4)">捐赠一分钱</li>
        </ul>
      </div>
    </div>
    <div class="shadow">

    </div>
    <div class="baseheader">

    </div>

  </div>

</template>

<script>
  import $ from 'jquery/dist/jquery.min'

  export default {
        name: "Rheader",
        data() {
            return {}
        },
    methods:{
      initAnimate:function (Y) {
        $(window).scroll(function(){
          var scroll=$(window).scrollTop();
          if(0.5*Y<=scroll && scroll<=2*Y) {
            $("ul li").css("color","black");
            $("ul li:nth-of-type(1)").css("color","white")

          }else if(2*Y<=scroll && scroll<=4.5*Y) {
            $("ul li").css("color","black");
            $("ul li:nth-of-type(2)").css("color","white")

          }else if(scroll>=4.5*Y && scroll<=6.5*Y){
            $("ul li").css("color","black");
            $("ul li:nth-of-type(3)").css("color","white")

          }else if(scroll>=6.5*Y){
            $("ul li").css("color","black");
            $("ul li:nth-of-type(4)").css("color","white")
            $("ul li:nth-of-type(5)").css("color","white")

          } else {
            $("ul li").css("color","black");
//            $("ul li:nth-of-type(1)").css("color","white")
          }
        })
      },
      jumpto(n){
        var Y = $(window).height();
        switch (n){
          case 1:
            $("html,body").animate({scrollTop: 0.8*Y+"px"}, 800);
            break;
          case 2:
            $("html,body").animate({scrollTop: 4.1*Y+"px"}, 800);
            break;
          case 3:
            $("html,body").animate({scrollTop: 5*Y+"px"}, 800);
            break;
          case 4:
            $("html,body").animate({scrollTop: 6.54*Y+"px"}, 800);
            break;
        }
      },
      outWindow(){
        $('#form').hide();
        this.$emit("transfer");
      }
    },
    created: function () {
      var Y = $(window).height()
      this.initAnimate(Y);
    },
    }
</script>


<style scoped>
  li{
    transition: 0.3s;
    font-family: "PingFang SC","Microsoft JhengHei";
  }
  .baseheader{
    background-color: white;
    /*box-shadow: 1px 1px 2px red;*/
    box-sizing: border-box;
    position: fixed;
    top: 0px;
    z-index: 9997;
    width: 96%;
    left: 2%;
    height: 58px;
    margin-top: 1rem;
  }
  .Rheader{
    background-color: transparent;
    /*box-shadow: 1px 1px 2px red;*/
    box-sizing: border-box;
    position: fixed;
    top: 0px;
    z-index: 9999;
    border: 2px solid black;
    width: 96%;
    left: 2%;
    height: 58px;
    margin-top: 1rem;
  }
  .shadow{
    background: -webkit-linear-gradient(to right, red, #e6e4e6); /* Safari 5.1 - 6.0 */
    background: -o-linear-gradient(right, red, #e6e4e6); /* Opera 11.1 - 12.0 */
    background: -moz-linear-gradient(right, red, #e6e4e6); /* Firefox 3.6 - 15 */
    background: linear-gradient(to right, red, #e6e4e6); /* 标准的语法 */
    box-sizing: border-box;
    position: fixed;
    top: 0.8rem;
    z-index: 9998;
    width: 96%;
    left: calc(2% + 0.45rem);
    height: 58px;
    margin-top: 1rem;
  }
  div.left{
    background-color: transparent;
    padding-top: 5px;
    text-align: center;
    display: inline-block;
    width: 70px;
    line-height: 12px;
    border-right: 2px solid black;
    height: 50px;

  }
  span.line{
    display: inline-block;
    width: 35px;
    height: 5px;
    background: black;
  }
  div.center ul{
    background-color: transparent;
    padding-left: 0;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    /*display: inline-block;*/
  }
  div.center{
    background-color: transparent;
    position: relative;
    top: -10px;
    height: 56px;
    display: inline-block;
    width: 90%;
    /*border-right: 2px solid black;*/
  }
  div.center ul li{
    background-color: transparent;
    list-style: none;
    display: inline-block;
    cursor: pointer;
  }
  #app > div > div:nth-child(1) > div.Rheader > div.center > ul > li:hover{
    color: white;
  }
  div.right{
    background-color: transparent;
    position: absolute;
    right: 0;
    display: inline-block;
  }
  div.right img{
    padding-top: 12px;
    padding-right: 25px;
    height: 30px;
  }

</style>
