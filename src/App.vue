<template>
  <div id="app">
    <HelloWorld msg="Welcome To Photo"/>
    <p>By Patcharapa Chaitap</p>
    <div class="container col-11">
      <div class="card-body" style="background-image: url(image/c51eefd6458889941fff518c31e924b4.jpg);">
        <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
          <ol class="carousel-indicators">
            <li data-target="#carouselExampleIndicators" data-slide-to="0" class=""></li>
            <li data-target="#carouselExampleIndicators" data-slide-to="1" class="active"></li>
            <li data-target="#carouselExampleIndicators" data-slide-to="2" class=""></li>
          </ol>
          <div class="carousel-inner">
          <div class="carousel-item">
            <img class="d-block w-100" src="./assets/110.png" alt="First slide">
          </div>
          <div class="carousel-item active">
            <img class="d-block w-100" src="./assets/4.png" alt="Second slide">
          </div>
          <div class="carousel-item">
            <img class="d-block w-100" src="./assets/23.png" alt="Third slide">
          </div>
        </div> 
        <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
          <span class="carousel-control-custom-icon" aria-hidden="true">
            <i class="fas fa-chevron-left"></i>
          </span>
          <span class="sr-only">Previous</span>
        </a>
        <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
          <span class="carousel-control-custom-icon" aria-hidden="true">
            <i class="fas fa-chevron-right"></i>
          </span>
        <span class="sr-only">Next</span>
        </a>
      </div>
    </div>
  </div>

    
    <br><hr>
  <div class="container">
    <div class="row" style="background-color: rgb(184, 197, 190);">
        <!-- 2. รับค่าจาก emall @cc แล้วส่งไปทำงานใน function "sum"-->
        <div class="col-6"><br><img alt="รูป" width="50%" src="./assets/3.jpg"><br><br><Counter lable=""  @cc="sum" /></div>
        <div class="col-6"><h1>{{total}}</h1></div>
      </div>
      <hr>
      <div class="row" style="background-color: rgb(184, 197, 190);">
        <div class="col-6"><br><img alt="รูป" width="50%" src="./assets/2.jpg"><br><br><Counter lable=""  @cc="sum1" /></div>
       <div class="col-6"><h1>{{total1}}</h1></div>
      </div>
      <hr>
      <div class="row" style="background-color: rgb(184, 197, 190);">
        <div class="col-6"><br><img alt="รูป" width="50%" src="./assets/7.jpg"><br><br><Counter lable=""  @cc="sum2" /></div>
        <div class="col-6"><h1>{{total2}}</h1></div>
      </div>
      <hr>
      <br>
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
  font-family: "Comic Sans MS", cursive, sans-serif;
  background-image: url(./assets/42.jpg);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #4a84be;
  margin-top: 60px;
}
</style>
