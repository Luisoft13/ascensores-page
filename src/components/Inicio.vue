<template>
  <b-carousel
    id="carousel-1"
    v-model="slide"
    :interval="3000"
    fade
    indicators
    background="#ccc"
    img-width="1024"
    img-height="480"
    style="text-shadow: 1px 1px 2px #000;"
  >
    <!-- Slides with custom text -->
    <b-carousel-slide>
      <template v-slot:img>
        <img
          class="content_slider"
          width="1024"
          height="480"
          :src="require('@/assets/images/Inicio/slider-1.jpg')"
          alt="image slot"
        >
        <div class="carousel-caption">
          <h1 class="mt-5">MODERNIZACION</h1>
          <div class="linea"></div>
          <p>Modernizamos la tecnología</p>
          <p>de su ascensor mejorando el confort</p>
        </div>
      </template>
    </b-carousel-slide>

    <!-- Slides with img slot -->
    <!-- Note the classes .d-block and .img-fluid to prevent browser default image alignment -->
    <b-carousel-slide>
      <template v-slot:img>
        <img
          class="content_slider"
          width="1024"
          height="480"
          :src="require('@/assets/images/Inicio/slider-2.jpg')"
          alt="image slot"
        >
        <div class="carousel-caption">
          <h1 class="mt-5">SOMOS ESPECIALISTAS</h1>
          <div class="linea"></div>
          <p>En instalación, mantenimiento</p>
          <p>y reparación</p>
        </div>
      </template>
    </b-carousel-slide>
    <b-carousel-slide>
      <template v-slot:img>
        <img
          class="content_slider"
          width="1024"
          height="480"
          :src="require('@/assets/images/Inicio/slider-3.jpg')"
          alt="image slot"
        >
        <div class="carousel-caption mb-25">
          <h1 class="mt-5">VENTAS DE ASCENSORES</h1>
          <div class="linea"></div>
        </div>
      </template>
    </b-carousel-slide>
  </b-carousel>
</template>

<script>
  export default {
    data() {
      return {
        slide: 0,
        sliding: null
      }
    },
    methods: {
      onSlideStart() {
        this.sliding = true
      },
      onSlideEnd() {
        this.sliding = false
      }
    }
  }
</script>
<style>
.content_slider {
  height: 100vh;
  width: 100%;
  filter: brightness(0.50);
}
.carousel-caption h1{
  text-align: right;
  font-size: 80px; font-weight: 700; line-height: 80px;
}
.carousel-caption{
  right: 10%;
}
.carousel-caption p{
  color: white;
  font-size: 30px;
  text-align: right;
  opacity: 1;
}
.linea {
  border-top: 3px solid white;
  height: 2px;
  max-width: 250px;
  padding: 0;
  margin: 20px 5px 0 auto;
  text-align: right;
}
@media (max-width: 768px) {
  .carousel-inner img {
      height: 100vh;
  }
  .carousel-caption{
      bottom: 80px;
  }
  .carousel-caption p{
      font-size: 20px;
  }
  .carousel-caption h1 {
    font-size: 30px; line-height: normal;
  }
}
</style>
