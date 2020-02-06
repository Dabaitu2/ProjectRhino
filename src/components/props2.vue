<template>
  <div class="main">
    <div class="head2window">
      <div class="header">
        <div class="title">
          <img src="../assets/getMoney.png" alt="" class="icon">
        </div>
        <div class="bottombar">
          <span class="iconBox">
          <img src="../assets/icon-cross(2).png" alt="" class="bottomItem">
          </span>
          <span class="digital">
          <slot name="info02"></slot>
            </span>
          <span class="iconBox item2">
          <img src="../assets/icon-cross(2).png" alt="" class="bottomItem ">
          </span>
        </div>
      </div>
      <div class="body">
        <div class="bodycontainer">
          <p class="para">
            也许你希望为保护事业做点什么<br>
            积少成多，滴水成河<br>
            你的捐赠就是在为犀牛保护助力
          </p>
          <p class="para" style="font-family: Me; color: red; font-weight: 400">
            Maybe you want to do something<br>
            Many a little makes a mickle<br>
            Your forwarding is protecting rhino
          </p>
        </div>
      </div>
      <div class="footer">
        <div class="innerframe"><slot name="btnInfo02"></slot></div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "",
    data() {
      return {}
    }
  }
</script>


<style scoped>
  .main{
    position: relative;
  }
  .courier{
    font-family: "Courier New";
    color: red;
    font-weight: 800;
  }
  .digital{
    text-align: center;
    display: inline-block;
    font-family: "FangZheng8bit";
    color: red;
    font-size: 1rem;
    width: 23rem;
  }
  .head2window{
    width: 28rem;
    border: 2px solid black;
    height: 32rem;
    margin: 0 auto;
    z-index: 3;
    background-color: white;
    overflow: hidden;
  }


  div.header{
    /*text-align: left;*/
    text-align: center;
    padding: 0;
    height: 5.5rem;
    background: url("../assets/redDot.png") repeat;
    -webkit-background-size: 146%;
    background-size: 146%;
    border-bottom: 2px solid black;
  }
  div.title{
    text-align: center;
    /*margin-left: 1rem;*/
    border-radius: 6px;
    background-color: #fff;
    margin-top: 1rem;
    display: inline-block;
    width: 50%;
    height: 3.3rem;
    border: 2px solid black;
    color: red;
    font-size: 1.2rem;
    font-family: FangZheng8bit;
  }
  img.icon{
    position: relative;
    top: 0.15rem;
    margin-top: 0.35rem;
    height: 2.3rem;
  }
  div.closebar{
    overflow: hidden;
    margin-top: 1.5rem;
    position: relative;
    height: 3rem;
    border-bottom: 2px solid black;
  }
  div.bottombar{
    top: 5.75rem;
    text-align: left;
    width: 28rem;
    overflow: hidden;
    height: 1.6rem;
    position: absolute;
    border-bottom: 2px solid black;

  }
  .closebar>span:nth-of-type(1){
    position: relative;
    top: 1.2rem;
    left: 1.2rem;
  }
  div.bodycontainer{
    margin-top: 2rem;
    padding: 2.2rem;
    /*padding-top: 0.6rem;*/
    font-family: "PingFang SC";
  }
  p.para{
    font-size: 1.14rem;
    /*text-align: left;*/
    /*text-indent: 2rem;*/
    text-align: center;
    margin-bottom: 2rem;
  }
  span.iconBox{
    text-align: center;
    display: inline-block;
    height: 1.6rem;
    border-right: 2px solid black;
    width: 2rem;
  }
  img.bottomItem{
    padding-top: 0.35rem;
    height: 0.9rem;
  }
  span.item2{
    float: right;
    /*transform: ;*/
    transform-style: preserve-3d;
    transform: rotateY(180deg);
  }
  div.footer{
    position: absolute;
    bottom: 0;
    height: 4.4rem;
    width: 28rem;
    box-sizing: border-box;
    background-color: black;
    padding: 0 2px;
    padding-top: 2px;
  }
  div.innerframe{
    width: 27.8rem;
    height: 4rem;
    box-sizing: border-box;
    border: 3px solid white;
    background-color: black;
    font-family: FangZheng8bit;
    color: white;
    line-height: 3.8rem;
    font-size: 1.8rem;
    font-weight: 400;
    text-align: center;
    letter-spacing: 1rem;
  }
</style>
