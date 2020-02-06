<template>
  <div class="main">
    <div class="shadowbox"></div>
    <div class="shadowbox"></div>
    <div class="head2window">
      <div class="header">
        <div class="title">
          <img src="../assets/icon-doc.png" alt="" class="icon">
          <slot name="title"></slot>
        </div>
        <div class="closebar">
            <span class="courier">
              <slot name="desc"></slot>
            </span>
          <span class="close">&times;</span>
        </div>
      </div>
      <div class="body">
        <div class="bodycontainer">
          <p class="para">
            <slot name="cndetail"></slot>
          </p>
          <p style="text-align: right; position: relative; top: -1rem;">
            <slot name="cnAuthor"></slot>
          </p>
          <p class="para" style="font-family: Me">
            <slot name="Endetail"></slot>
          </p>
          <p style="text-align: right; position: relative; top: -1rem; font-family: Me" >
            <slot name="EnAuthor"></slot>
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
.head2window{
  width: 50rem;
  border: 2px solid black;
  height: 32rem;
  position: relative;
  margin: 0 auto;
  z-index: 3;
  top: -63rem;
  background-color: white;

}
.shadowbox{
  width: 50rem;
  background-color: #00d600;
  height: 31.5rem;
  position: relative;
  left: 3.4rem;
  z-index: 2;
  opacity: 0.4;
}
.shadowbox:nth-of-type(2){
  width: 50rem;
  background-color: #d62000;
  height: 31.5rem;
  position: relative;
  left: 3rem;
  z-index: 1;
  top: -30.5rem;
  opacity: 0.4;
}

  div.header{
    text-align: left;
    padding: 0;
    height: 4rem;
    background: url("../assets/bgdot.png") repeat;
    -webkit-background-size: 126%;
    background-size: 126%;
    border-bottom: 2px solid black;
  }
  div.title{
    text-align: center;
    margin-left: 1rem;
    border-radius: 6px;
    background-color: #fff;
    margin-top: 1rem;
    display: inline-block;
    width: 40%;
    height: 2rem;
    border: 2px solid black;
    color: red;
    font-size: 1.2rem;
    font-family: FangZheng8bit;
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
</style>
