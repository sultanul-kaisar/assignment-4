<script setup>
const images =[
  {
    id:1,
    title:"Slider 1",
    thumbnail:"/images/slider1.jpg",
  },
  {
    id:2,
    title:"slider 2",
    thumbnail:"/images/slider2.jpg",
  },
  {
    id:3,
    title:"Slider 3",
    thumbnail:"/images/slider3.jpg",
  },
  {
    id:2,
    title:"slider 4",
    thumbnail:"/images/slider4.jpg",
  },{
    id:1,
    title:"Slider 5",
    thumbnail:"/images/slider5.jpg",
  },
];




</script>


<template>
  <div id="carouselExampleControls" class="carousel slide" data-bs-ride="carousel">
    <div class="carousel-inner">
      <div v-for="(image, index) in images" :key="index" :class="['carousel-item', index === 0 ? 'active' : '']">
        <img :src="image.thumbnail" class="d-block w-100" alt="Carousel Image">
      </div>
    </div>
    <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>
</template>



<style scoped>

.carousel{
  height: 800px;
  width: 1200px;
  overflow: hidden;
}

.carousel-control-prev{
  padding-bottom: 200px;
  color: aqua;
}
.carousel-control-next{
  padding-bottom: 200px;
  color: aqua;
}
img{
  height: 500px;
  width: 1200px;
}
</style>