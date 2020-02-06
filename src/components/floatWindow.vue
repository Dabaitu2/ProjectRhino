<template>
  <div class="main">
    <img src="../assets/coin.png" alt="" class="shrink" @click="WindowOut">
    <div class="head2window" id="small">
      <div class="header">
        <span class="close">
          <img src="../assets/heart.png" alt="" style="width: 2rem;" @click="windowClose">
        </span>
      </div>
      <div class="body">
        <div class="line_01">
          <div class="transfer" @click="handleTransfer">
            转发助力
          </div><div class="donate" @click="handleDonate">
            捐赠爱心
          </div>
        </div>
        <p class="red" style="font-family: 'Courier New'">Each change matters</p>
        <div class="more">
          <!--<img src="../assets/us.png" alt="" >-->
        </div>
        <div class="moreMoney">
          <!--<div class="circle">-->
            $
          </div>
        </div>
      </div>
    </div>
  </div>

</template>

<script>
  import $ from 'jquery/dist/jquery.min'
  export default {
    name: "",
    data() {
      return {}
    },
    methods:{
      handleTransfer() {
        this.$emit("transfer")
        $('#form').hide();
      },
      handleDonate(){
//        $('.moreMoney').slideToggle();
      },
      WindowOut(){
        $('#small').show();
        $('.shrink').hide()
      },
      windowClose(){
        $('.shrink').show()
        $('#small').toggle();
      }
    }
  }
</script>


<style scoped>
  img{
    transition: 0.3s;
    cursor: pointer;
  }
  .red{
    color: red;
    font-family: FangZheng8bit;
    font-size: 1rem;
    padding-left: 1rem;
    font-weight: 600;
  }
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
    position: fixed;
    top: 8rem;
    right:2rem;
    z-index: 9999;
  }
  .head2window{
    display: none;
    width: 13rem;
    border: 3px solid black;
    /*height:8rem;*/
    margin: 0 auto;
    z-index: 3;
    background-color: white;
    animation: enlarge 0.4s ease;
  }
  div.more{
    display: none;
    /*padding:0 2rem;*/
    text-align: center;
    padding-bottom: 1rem;
  }
  div.more img{
    margin: 0 auto;
    width: 8rem;
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
  span.close{
    box-sizing: border-box;
    float: right;
    background-color: white;
    height: 2.1rem;
    line-height:1.5rem;
    font-size: 2.2rem;
    border: 2px solid black;
    border-left: 3px solid black;
    position: relative;
    top: -1px;
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


  .title span{
    font-size: 2rem;
    line-height: 3rem;
    letter-spacing: 5px;
    animation: shine 2s linear infinite
  }
div.line_01{
  cursor: pointer;
  background-color: #5a5a5a;
  height: 2.3rem;
  box-sizing: border-box;
  border: 2px solid black;
  padding: 0;
}
  div.transfer{
    text-align: center;
    height: 2rem;
    display: inline-block;
    width: 50%;
    box-sizing: border-box;
    border: 3px solid white;
    background-color: black;
    color: white;
    font-family: FangZheng8bit;
    line-height: 1.6rem;
  }
  div.donate{
    height: 2.1rem;
     display: inline-block;
     width: 50%;
     box-sizing: border-box;
     border: 3px solid #000000;
     border-left: 6px solid #000000;
     border-bottom: 4px solid #000000;
    color: black;
    background-color: #fff;
    font-family: FangZheng8bit;
    line-height: 1.6rem;
    text-align: center;
   }
  div.moreMoney{
    text-align: center;
    padding-bottom: 1rem;
    display: none;
  }
  div.circle{
    line-height: 4rem;
    text-align: center;
    font-size: 3rem;
    color: #ff7c29;
    display: inline-block;
    width: 4rem;
    height: 4rem;
    border-radius: 50%;
    background-color: #ffc61e;
    box-shadow: 2px 0px 0px #80671d;
  }
 @keyframes bounce {
   0%{
     position: relative;
     top: 0;
   }
   50%{
     position: relative;
     top: -20px;
   }
   100%{
     position: relative;
     top: 0;
   }
 }
  img.shrink{
    cursor: pointer;
    width: 5rem;
    margin-top: 2rem;
    animation: bounce 1.2s ease infinite;
    padding-right: 2rem;
    /*display: none;*/
  }
  @keyframes enlarge {
    from{
      width: 0;
      height: 0;
    }
    to{

    }
  }

</style>

