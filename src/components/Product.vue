<template>
  <div class="mainForm" v-if="finished" id="form">
    <div class="prodForm" id="divForm" v-show="finished">
        <div class="innerform">
          <div class="headPart">
            <div class="headline01">
              <span class="Me red" style="line-height: 2.5rem;">xixi4rhino</span>
            </div>
            <div class="headline02">
              <h1 class="digit" style="line-height:4.5rem;">来自陌生<span class="red">xi</span>的讯息</h1>
            </div>
            <div class="headline03">
              <span class="Me" style="line-height: 2.5rem;">Time: {{time}}</span>
              <span class="Me" style="line-height: 2.5rem; padding-left: 0;">IP: {{ip}}</span>
            </div>
          </div>
          <div class="bottomPart">
            <div class="leftpart">
              <p>{{name}}接收到一条署名“xixi4rhino”的神秘讯息。
                </p><p>{{name}}从黑暗中英勇拯救了带角的不明生物！
                </p><p>{{name}}看到还有很多正在等待救援的眼睛。
                </p><br>
              <p>{{name}}决定邀请充满爱与勇气的你，一起探索<span class="red">“xixi4rhino”</span>的秘密！
              </p>
              <div class="codeBar" @click="canvas">
                <img src="../assets/us.png" alt="" class="code">
              </div>
            </div>
          </div>
        </div>
    </div>
  </div>
</template>

<script>
  import $ from 'jquery/dist/jquery.min'
  import html2canvas from 'html2canvas'
  import axios from 'axios'
  var instance = axios.create({
    baseURL: 'http://pv.sohu.com',
    timeout: 6000,
  });

    export default {
        name: "",
        data() {
            return {
              time: "2018/04/13 14:00",
              ip: "",
              name: "XXX",
              finished: false
            }
        },
        props:['Supername'],
      watch:{

        'Supername'(to, from){
          $('#form').show();
          this.name = to;
          this.finished = true;
          $(".trans").toggle()
          this.canvas()
        }
      },
      created(){

        this.update()

      },
      methods:{
        canvas(){
          var that = this;
          $("canvas").remove()
          $('#divForm').show();
          html2canvas(document.querySelector("#form")).then(canvas => {

            $(".mainForm").append(canvas);
            $('#divForm').hide();
//            console.log($("canvas").length)
          });
        },
        update(){
          this.time = new Date().toLocaleString().replace("上午"," ")
          this.ip = document.cookie.split(";")[0].split("=")[1]
        }
      }
    }
</script>


<style scoped>
  .digit{
    font-family: FangZheng8bit;
  }
  .Me{
    font-family: Me;
  }
  .red{
    color: red;
  }
    div.prodForm{
      position: relative;
      left: -4.7rem;
      top: -6.3rem;
      text-align: center;
      padding: 3rem;
      display: inline-block;
      background-color: white;
      /*border: 2px solid black;*/
      width: 34rem;
      height:48.6rem;
      background: url("../assets/prodBg.png") no-repeat;
      background-size:98.6%;
      transform: scale(0.77);
    }
  div.innerform{
    overflow: hidden;
    text-align: left;
    box-sizing: border-box;
    border: 5px solid black;
    height: 48rem;
    width: 33rem;
    background-color: white;
  }
  div.headline01{
    padding-left: 1.5rem;
    height: 2.5rem;
    border-bottom: 3px solid black;
  }
    div.headline02{
      text-align: center;
      height: 6rem;
      border-bottom: 3px solid black;
    }
    div.headline03{
      height: 2.5rem;
      border-bottom: 3px solid black;
      display: flex;
      flex-direction: row;
      justify-content: space-between;
    }
    .headline03 span:nth-of-type(1){
      padding-left: 1.5rem;
    }
  .headline03 span:nth-of-type(2){
    padding-right: 1.5rem;
  }
  div.bottomPart div{
    display: inline-block;

  }
  div.leftpart{
    position: relative;
    padding: 1rem;
    border-right: 2px solid black;
    /*box-sizing: border-box;*/
    /*margin-top: 3rem;*/
    /*padding-top: 3rem;*/
    /*top: -11.9rem;*/
    width: 27.2rem;
    height: 36.6rem;
    font-family: Me, "PingFang SC", "Microsoft YaHei UI", "Microsoft JhengHei", FangZheng8bit;
  }
  div.leftpart p{
    position: relative;
    /*top: -3rem;*/
    padding-right: 2rem;
    padding-left: 3rem;
    font-size: 1.2rem;
    text-indent: 2rem;
  }

  div.rightpart{
    width: 3rem;
    border-left: 3px solid black;
    height: 36.1rem;
  }
  div.codeBar{
    display: inline-block;
    width: 7rem;
    border: 2px solid black;
    position: absolute;
    bottom: 4rem;
    left: -0.1rem;

  }
  img.code{
    width: 7rem;
  }
  div.rightpart{
  }
  div.bottomPart{
    background: url("../assets/verti.png") right no-repeat;
    background-size:14.3%;
    background-position: 28.6rem -0.1rem;
  }
  #form{
    /*display: none;*/
  }
  .mainForm{
    display: inline-block;
    position: fixed;
    top: 2rem;
    left: 28rem;
    height: 42rem;
    width: 30rem;
    background-color: #ffffff;
    z-index: 99999;
  }
  .result{
    height: 26rem;
    width: inherit;
  }

</style>
