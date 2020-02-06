<template>
  <div class="main">
    <div class="head2window">
      <div class="header">
      </div>
      <div class="body">
        <div class="bodycontainer">
          <p>
            1922年，中国的最后一只犀牛因人类猎杀<span class="red">灭绝；</span><br>
            2014以来，南非平均每年1050头犀牛惨遭<span class="red">偷猎；</span><br>
            2018年3月20日，世界上仅存的北部白犀牛“苏丹”离世，北部白犀牛理论<span class="red">灭绝；</span><br>
            如果猎杀犀牛的势头不能得到有效遏制，到2026年南非的犀牛将<span class="red">灭绝。</span>
          </p>
          <p style="padding-top: 2rem; color: red">
            Rhino“is disappearing” day by day in different corners of our planet.
          </p>
        </div>
      </div>
      <div class="footer">
        <div class="bottombar">
          <span class="iconBox">
          <img src="../assets/icon-cross(2).png" alt="" class="bottomItem">
          </span>
          <span class="iconBox reverse">
          <img src="../assets/icon-cross(2).png" alt="" class="bottomItem">
          </span>
          <span class="iconBox right">
                      <img src="../assets/icon-arrow.png" alt="" class="bottomItem">
          </span>
          <span class="iconBox right">
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
  .red{
    color: red;
  }
  .main{
    position: relative;
  }
  .head2window{
    width:65%;
    border: 3px solid black;
    height: 22rem;
    position: absolute;
    margin: 0 auto;
    z-index: 3;
    top: 27.5rem;
    /*top: -63rem;*/
    background-color: white;
    left: 17.5%;

  }

  div.header{
    background: url("../assets/greenLine.png") repeat;
    background-size:120%;
    text-align: left;
    padding: 0;
    height: 2.2rem;
    border-bottom: 2px solid black;
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
    width: 100%;
    overflow: hidden;
    height: 1.6rem;
    position: absolute;
    bottom: 0;
    border-top: 2px solid black;
  }
  span.close{
    height: 2.2rem;
    line-height:2rem;
    position: absolute;
    right: 0;
    font-size: 2rem;
    border-left: 2px solid black;
    background-color: #fff;
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
    padding: 2.2rem 8rem;
    font-family: "PingFang SC";
    text-align: center;
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
  span.right:nth-of-type(4){
    /*margin-left: 88.6%;*/
    border-left: 2px solid black;
    border-right: 0;
  }
  span.right:nth-of-type(4) img{
    transform-style: preserve-3d;
    transform: rotateY(180deg);
  }
  span.right:nth-of-type(3){
    margin-left: 88.6%;
    border-left: 2px solid black;
    border-right: 0;
  }
  span.right:nth-of-type(3) img{
    transform-style: preserve-3d;
    transform: rotateY(180deg);
  }
  p{
    font-family: 'Me','PingFang SC',"Microsoft JhengHei UI";
    font-size: 1.1rem;
    display: inline-block;
    margin: 0 auto;
    line-height: 2.2rem;
    color: black;
  }
  span.reverse{
    float: right;
    transform-style: preserve-3d;
    transform: rotateY(180deg);
  }
</style>
