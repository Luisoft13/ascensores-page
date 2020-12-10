<template>
<div class="container">
    <VueSlickCarousel
        v-bind="slickSettings"
        class="slick-carousel"
      >
        <div
            v-for="image in images"
            :key="image.id"
        >
            <b-card class="mr-2 ml-2">
                    <b-img
                        class="content_img"
                        :src="image.url"
                    />
                    <div class="mt-3">
                        <p class="content-img_title">{{image.title}}</p>
                        <b-button href="#" variant="primary">Ver más</b-button>
                    </div>
            </b-card>
        </div>
      </VueSlickCarousel>
    </div>
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
        speed:250,
        slidesToShow: 3,
        slidesToScroll: 3,
        initialSlide:0,
        responsive: [
          {
            breakpoint: 1024,
            settings: {
              slidesToShow: 3,
              slidesToScroll: 3,
              infinite: false,
              dots: false
            }
          },
          {
            breakpoint: 600,
            settings: {
              slidesToShow: 2,
              slidesToScroll: 2,
              initialSlide: 2
            }
          },
          {
            breakpoint: 400,
            settings: {
              slidesToShow: 1,
              slidesToScroll: 1,
            }
          }
        ]
      },
      images: [
            { id: 1, url: require('@/assets/images/servicios/servicios_1.png'), title: 'VENTAS DE ASCENSORES' },
            { id: 2, url: require('@/assets/images/servicios/servicios_2.png'), title: 'INSTALACIÓN' },
            { id: 3, url: require('@/assets/images/servicios/servicios_3.jpg'), title: 'MANTENIMIENTO' },
            { id: 4, url: require('@/assets/images/servicios/servicios_4.jpg'), title: 'EMERGENCIA' },
            { id: 5, url: require('@/assets/images/servicios/servicios_5.jpg'), title: 'REPARACIONES' },
            { id: 6, url: require('@/assets/images/servicios/servicios_6.jpg'), title: 'MODERNIZACIÓN' },
        ],

    }
  },
}
</script>
<style>
.content_img {
    height: 250px !important;
    width: 100%;
}
.content-img_title {
    font-size: 23px;
}
</style>
