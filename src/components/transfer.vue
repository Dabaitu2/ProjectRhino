<template>
  <div class="main" id="newBox">
    <div class="shadowbox"></div>
    <div class="head2window">
      <div class="header">
        <div class="title">
          <img src="../assets/book.png" alt="" class="icon">
          转发说明
        </div>
        <div class="closebar">
          <span class="close leftone" @click="close">
            <img src="../assets/heart.png" alt="" class="closeItem">
          </span>
            <span class="courier" style="position: relative; top: 1.2rem">
              Forwarding Instruction
            </span>
          <span class="close" @click="close">
            <img src="../assets/heart.png" alt="" class="closeItem">
          </span>
        </div>
      </div>
      <div class="body">
        <div class="bodycontainer">
          <div class="searchbar">
            <input type="text" v-model="name" class="searchInput" placeholder="请输入你的名字 Enter your name">
            <span class="next" @click="getProduct">
            </span>
          </div>
          <p>每一份关注都值得被记录<br>
            我们将生成专属于你的转发简讯</p>
          <p style="font-family: Me">
            Every concern deserves to be recorded
            We will generate forwarding message for you
          </p>
        </div>
      </div>
      <div class="footer">
        <div class="bottombar">
          <span class="iconBox">
          <img src="../assets/icon-cross(2).png" alt="" class="bottomItem">
          </span>
          <span class="iconBox item2">
          <img src="../assets/icon-cross(2).png" alt="" class="bottomItem ">
          </span>
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
      return {
        name:""
      }
    },
    methods:{
      getProduct(){
        var that = this;
        this.$emit("name",{name:that.name})
      },
      close(){
        $(".trans").hide()
      }
    }
  }
</script>


<style scoped>
  .main{
    position: fixed;
    top:10rem;
    left: 28rem;
    z-index: 9999;
  }
  .courier{
    font-family: "Courier New";
    color: red;
    font-weight: 800;
  }
  .head2window{
    width: 30rem;
    border: 2px solid black;
    height: 22rem;
    margin: 0 auto;
    z-index: 3;
    background-color: white;
    position: relative;
    top: -22.8rem;
    box-shadow: 5px 5px 0 rgba(255, 0, 0, 0.42);
  }
  .shadowbox{
    width: 30rem;
    background-color: #00d600;
    height: 22rem;
    position: relative;
    z-index: 2;
    opacity: 0.4;
    left: 0.8rem;
  }

  div.header{
    text-align: center;
    padding: 0;
    height: 4rem;
    background: url("../assets/bgdot.png") repeat;
    -webkit-background-size: 126%;
    background-size: 126%;
    border-bottom: 2px solid black;
  }
  div.title{
    text-align: center;
    /*margin-left: 1rem;*/
    border-radius: 6px;
    background-color: #fff;
    margin-top: 1rem;
    display: inline-block;
    width: 60%;
    height: 2rem;
    border: 2px solid black;
    color: red;
    font-size: 1.2rem;
    font-family: FangZheng8bit;
    line-height: 2rem;
  }
  img.icon{
    position: relative;
    /*top: 0.2rem;*/
    /*margin-top: 0.1rem;*/
    width: 1.3rem;
    left: -2rem;
  }
  img.closeItem{
    position: relative;
    top: 0.2rem;
    width: 2rem;
  }
  span.leftone{
    display: inline-block;
    float: left;
    border-left: 0 !important;
    border-right: 2px solid black;
    position: relative;
    top: 0.85rem !important;
    left: 0 !important;
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
    top: 0.8rem;
    line-height:2rem;
    position: absolute;
    right: 0;
    font-size: 2rem;
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
    margin-top: 2rem;
    padding: 2.2rem;
    font-family: "PingFang SC";
    text-align: center;
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
  span.item2{
    float: right;
    /*transform: ;*/
    transform-style: preserve-3d;
    transform: rotateY(180deg);
  }
  .searchbar{
    /*box-sizing: border-box;*/
    display: inline-block;
    width: 20rem;
    height: 2rem;
    border: 2px solid black;
    border-radius: 6px;
    box-shadow: 3px 3px 0 #a4a4a4;
  }
  span.next{
    box-sizing: border-box;
    display: inline-block;
    width: 4rem;
    border-left: 2px solid black;
    height: 2rem;
    background: url("../assets/enter.png") no-repeat;
    background-size:40%;
    background-position: 1rem 0.5rem;
  }
  input.searchInput{
    font-family: "PingFang SC","Microsoft JhengHei","Microsoft YaHei UI";
    text-indent: 1rem;
    position: relative;
    top: -0.7rem;
    box-sizing: border-box;
    width: 15.5rem;
    height: 1.8rem;
    border: none;
    outline:none;
    margin: 0;
    margin-left:0.1rem;
    font-size: 0.8rem;
    color: #9b9b9b;

  }
  input.searchInput::placeholder{
    font-family: Me, "PingFang SC", "Microsoft YaHei UI";
    color: #9b9b9b;
  }
</style>
