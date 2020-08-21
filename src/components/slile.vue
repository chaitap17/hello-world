<template>
    <div class="container">
      <div id="carouselExampleControls" class="carousel slide" data-ride="carousel">
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img :src="img[0]"  />
          </div>
          <div class="carousel-item">
            <img :src="img[1]"  />
          </div>
          <div class="carousel-item">
            <img :src="img[2]"  />
          </div>
        </div>
        <a
          class="carousel-control-prev"
          href="#carouselExampleControls"
          role="button"
          data-slide="prev"
        >
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="sr-only">Previous</span>
        </a>
        <a
          class="carousel-control-next"
          href="#carouselExampleControls"
          role="button"
          data-slide="next"
        >
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="sr-only">Next</span>
        </a>
      </div>
    </div>

</template>
<script>
export default {
    data: function(){
        return{
            img:[
                require("./assets/2.jpg"),
                require("./assets/7.png"),
                require("./assets/23.jpg"),
            ],
        };
    },

};
</script>
<style>

</style>
