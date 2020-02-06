<template>
  <div v-if="!hasDone">
    <div class="smalltips">
      <div class="innerbox">
        <div class="closebar">
          <span @click="handleFinalClick">&times;</span>
        </div>
        <div class="body">
          <p>当所有的动物都灭绝，下一个会是谁?</p>
        </div>
      </div>
    </div>
    <div class="smalltips tips2" v-if="!step2">
      <div class="innerbox">
        <div class="closebar">
          <span @click="handleSecondClick">&times;</span>
        </div>
        <div class="body">
          <p>你为什么要无视?</p>
        </div>
      </div>
    </div>
    <div class="smalltips tips3" v-if="!step3">
      <div class="innerbox">
        <div class="closebar">
          <span @click="handleFirstClick">&times;</span>
        </div>
        <div class="body">
          <p>我们因为你将在2026年消失..</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "",
    data() {
      return {
        step2: false,
        step3: false,
        hasDone: true
      }
    },
    props:['state02'],
    watch: {
      'state02' (to, from) {
//          console.log("state changes!")
        this.hasDone = this.state02
      }
    },
    methods:{
      handleFirstClick(){
        this.step3 = true;
      },
      handleSecondClick(){
        this.step2 = true;
      },
      handleFinalClick(){
        this.hasDone = true;
        this.$emit('Step02_finished')
      }
    },
    created: function () {
      this.hasDone = this.state02
    }
  }
</script>


<style scoped>
  .smalltips{
    position: fixed;
    top: 20rem;
    padding: 1px;
    width: 24rem;
    height: 8rem;
    background-color: #fff;
    border: 1px solid gainsboro;
    left: calc(50% - 12rem);
  }
  .tips2{
    top: 19rem;
    left: calc(50% - 11rem);
  }
  .tips3{
    top: 18rem;
    left: calc(50% - 10rem);
  }
  .innerbox{
    border: 1px dashed grey;
    background-color: #fff;
    color: #5a5a5a;
    font-family:FangZheng8bit;
    font-size: 1.4rem;
    padding: 3px;
    height: 7.5rem;
  }
  .closebar span{
    float: right;
    border: 1px solid #000000;
    cursor: pointer;

  }
  .body{
    padding-top: 1.4rem;
    text-align: center;
  }
</style>
