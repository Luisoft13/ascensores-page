<template>
  <b-carousel
    id="carousel-1"
    v-model="slide"
    :interval="5000"
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
        <div class="carousel-caption content-carousel-1">
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
        <div class="carousel-caption content-carousel-2">
          <p style="font-size:36px">SOMOS</p>
          <h1>ESPECIALISTAS</h1>
          <div class="linea-2"></div>
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
        <div class="carousel-caption mb-25 content-carousel-3">
          <p style="font-size:36px">VENTAS DE </p>
            <h1>ASCENSORES</h1>
            <div class="linea-3"></div>
            <p>Contamos con ascensores</p>
            <p>modernos y a un buen precio</p>
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
.content-carousel-1 {
  display: block !important;
  text-align: right !important;
}
.content-carousel-2 {
  display: block !important;
  text-align: center !important;
}
.content-carousel-3 {
  display: block !important;
  text-align: left !important;
}
.carousel-caption h1{
  font-size: 80px; font-weight: 700; line-height: 80px;
}
.carousel-caption{
  right: 10%;
}
.carousel-caption p{
  color: white;
  font-size: 30px;
  opacity: 1;
}
.linea {
  border-top: 3px solid white;
  height: 2px;
  max-width: 250px;
  padding: 0;
  margin: 20px 5px 0 auto;
}
.linea-2 {
  border-top: 3px solid white;
  height: 2px;
  max-width: 250px;
  padding: 0;
  margin-left: auto;
  margin-right: auto;
}
.linea-3 {
  border-top: 3px solid white;
  height: 2px;
  max-width: 250px;
  padding: 0;
}
.carousel-indicators li {
    width: 20px !important;
    height: 20px !important;
    margin-right: 10px !important;
    margin-left: 10px !important;
    border-radius: 50%;
    opacity: 1 !important;
    background-color: white !important;
}
.carousel-indicators .active
{
    background-color:rgba(42, 209, 201, 0.4)!important;
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
