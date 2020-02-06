<template>
  <div class="main">
    <div class="head2window">
      <div class="header">
          <!--<span class="close">&times;</span>-->
      </div>
      <div class="body">
        <div class="bodycontainer">
          <div class="title">
           <span style="font-family: 'Courier New'; font-weight: 600"> WARNING!!!</span>
          </div>
          <div class="progressBar">
            <div class="bar">
              <img src="../assets/play.png" alt="" class="play">
            </div>
          </div>
        </div>
      </div>
      <div class="footer">
        <div class="bottombar">
          <span class="iconBox">
          <img src="../assets/icon-cross(2).png" alt="" class="bottomItem">
          </span>
          <span class="iconBox item2">
          <img src="../assets/icon-cross(2).png" alt="" class="bottomItem">
          </span>
        </div>
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
  @keyframes progress {
    from{
      width: 2rem;
    }
    to{
      width: 100%;
    }
  }
  @keyframes shine {
    0%{
      color: red;
    }
    50%{
      color: black;
    }
    100%{
      color: red;
    }
  }
  .main{
    position: relative;
  }
  .head2window{
    width: 25rem;
    border: 2px solid black;
    height: 15rem;
    margin: 0 auto;
    z-index: 3;
    background-color: white;

  }

  div.header{
    text-align: left;
    padding: 0;
    height: 2rem;
    background: url("../assets/redDot.png") repeat;
    -webkit-background-size: 140%;
    background-size: 140%;
    border-bottom: 2px solid black;
    overflow: hidden;
  }
  div.title{
    text-align: center;
    border-radius: 10px;
    background-color: #fff;
    margin-top: 1rem;
    display: inline-block;
    width: 80%;
    height: 3rem;
    border: 2px solid black;
    color: red;
    font-size: 1.2rem;
    font-family: FangZheng8bit;
    box-shadow: 4px 4px 0px #c3c1c3;
  }
  img.icon{
    position: relative;
    top: 0.15rem;
    margin-top: 0.1rem;
    width: 1.3rem;
  }
  div.closebar{
    overflow: hidden;
    margin-top: 0rem;
    position: relative;
    height: 3rem;
    border-bottom: 2px solid black;
  }
  div.bottombar{
    text-align: left;
    width: 25rem;
    overflow: hidden;
    height: 1.6rem;
    position: absolute;
    bottom: 0;
    border-top: 2px solid black;
  }
  span.close{
    float: right;
    background-color: white;
    height: 2.2rem;
    line-height:1.8rem;
    font-size: 2.2rem;
    border-left: 2px solid black;
  }
  span.digit{
    font-family: FangZheng8bit;
    color: red;
  }
  .closebar>span:nth-of-type(1){
    position: relative;
    top: 1.2rem;
    left: 1.2rem;
  }
  div.bodycontainer{
    padding: 0 auto;
    padding-top: 1rem;
    font-family: "PingFang SC";
  }
  p.para{
    font-size: 1.14rem;
    text-align: left;
    text-indent: 2rem;
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
  .title span{
      font-size: 2rem;
    line-height: 3rem;
    letter-spacing: 5px;
    animation: shine 2s linear infinite
  }
  .progressBar{
    display: inline-block;
    width: 18rem;
    border: 2px solid black;
    height: 2rem;
    margin-top: 1rem;
  }
  .progressBar .bar{
    text-align: left;
    width: 2rem;
    height: inherit;
    background-color: #ff2700;
    animation: progress 3s linear infinite

  }
  .play{
    margin-left: 0.5rem;
    height: 1.6rem;
    padding-top: 0.2rem;
  }
  span.item2{
    float: right;
    /*transform: ;*/
    transform-style: preserve-3d;
    transform: rotateY(180deg);
  }
</style>

