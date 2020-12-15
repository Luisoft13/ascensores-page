<template>
  <section id="servicio" class="content_proovedores">
  <div class="container text-center">
    <h2 class="content-title-proovedores">Proveedores</h2>
    <VueSlickCarousel
      v-bind="slickSettings"
      class="slick-carousel"
    >
      <div
        v-for="image in images"
        :key="image.id"
      >
        <b-img
            :src="image.url"
        />
      </div>
    </VueSlickCarousel>
  </div>
  </section>
</template>
<script>
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
export default {
  components: {
    VueSlickCarousel,
  },
  data: function () {
    return {
      slickSettings: {
        autoplay: true,
        dots: false,
        arrows:false,
        infinite: true,
        slidesToShow: 5,
        slidesToScroll: 5,
        initialSlide:0,
        responsive: [
          {
            breakpoint: 1024,
            settings: {
              slidesToShow: 5,
              slidesToScroll: 5,
              infinite: false,
              dots: false
            }
          },
          {
            breakpoint: 600,
            settings: {
              slidesToShow: 4,
              slidesToScroll: 4,
              initialSlide: 4
            }
          },
          {
            breakpoint: 400,
            settings: {
              slidesToShow: 2,
              slidesToScroll: 2,
            }
          }
        ]
      },
      images: [
        { id: 1, url: require('@/assets/images/proveedores/IMEM_01.png'),},
        { id: 2, url: require('@/assets/images/proveedores/IMEM_02.png'),},
        { id: 3, url: require('@/assets/images/proveedores/IMEM_03.png'),},
        { id: 4, url: require('@/assets/images/proveedores/IMEM_04.png'),},
        { id: 5, url: require('@/assets/images/proveedores/IMEM_05.png'),},
        { id: 6, url: require('@/assets/images/proveedores/IMEM_06.png'),},
        { id: 7, url: require('@/assets/images/proveedores/IMEM_07.png'),},
        { id: 8, url: require('@/assets/images/proveedores/IMEM_08.png'),},
      ],
      show: false,
    }
  },
}
</script>
<style>
.content_proovedores {
  padding: 120px 0;
  background: #e3e8ee;
}
.content-title-proovedores {
  font-size: 50px;
  padding-top: 20px;
  margin-bottom: 50px;
  color: #445b69;
  text-transform: uppercase;
  text-align: left;
}
@media (max-width: 768px) {
  h2 {font-size:35px !important; align-items: center !important;}
}
</style>
