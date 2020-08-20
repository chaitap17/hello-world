<template>
  <div id="app">
    <img src="./assets/logo.png" alt="">
    <HelloWorld msg="ชอบรูปไหนมากกว่ากัน?"/>
    <div class="col-12"><h1>{{total+total1+total2}}</h1></div>
    <br><hr>
    <div class="row">
        <!-- 2. รับค่าจาก emall @cc แล้วส่งไปทำงานใน function "sum"-->
      <div class="col-6"><br><img alt="รูป" width="40%" src="./assets/3.jpg"><br><br><Counter lable=""  @cc="sum" /><hr></div>
      <div class="col-6"><h1>{{total}}</h1></div>
      <div class="col-6"><br><img alt="รูป" width="40%" src="./assets/2.jpg"><br><br><Counter lable=""  @cc="sum1" /><hr></div>
      <div class="col-6"><h1>{{total1}} </h1></div>
      <div class="col-6"><br><img alt="รูป" width="40%" src="./assets/7.jpg"><br><br><Counter lable=""  @cc="sum2" /><hr></div>
      <div class="col-6"><h1 style="text-center">{{total2}} </h1></div>
    </div>
  </div>

  
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Counter from './components/Counter.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Counter,
  },
  
  data: function() {
      return {
          total: 0, // ผลรวมทั้งหมด --> เอาไปแสดงผล
          total1: 0,
          total2: 0,
      };
   },

  methods:{
  // 3.คำนวณผลรวมทั้งหมดที่ส่งออกมาจาก email
    // แล้วเก็บผลรวมไว้ที่ this.total
    sum(counterValue) {
      this.total = counterValue;
    },
    sum1(counterValue) {
      this.total1 = counterValue;
    },
    sum2(counterValue) {
      this.total2 = counterValue;
    },
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
