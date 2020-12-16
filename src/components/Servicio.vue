<template>
  <section id="servicio" class="content_servicios">
  <div class="container">
    <h2 class="content-title-section">Servicios</h2>
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
            <b-button class="content-btn_card" v-b-modal="'myModal' + image.id" ref="btnShow">Ver más</b-button>
          </div>
        </b-card>
      </div>
    </VueSlickCarousel>
    <div
      v-for="image in images"
      :key="image.id"
    >
        <b-modal :id="'myModal' + image.id" size="lg" hide-backdrop :title="image.title" centered>
          <div class="text-center">
            <p>
              {{ image.description }}
            </p>
            <b-img
              class="content-modal_image"
              :src="image.url"
            />
          </div>
          <template #modal-footer="{ close }">
            <div class="w-100">
              <b-button
                variant="success"
                size="sm"
                class="float-right mr-2 content-btn"
                href="https://api.whatsapp.com/send?phone=51 917937843&text=Hola *ASCENSORES PACIFIC S.A.C*, deseo más información acerca de este servicio."
                target="_blank"
                @click="close()"
              >
                Cotizar
                <img class="content-modal_icon" src="https://img.icons8.com/pastel-glyph/64/ffffff/whatsapp--v2.png"/>
              </b-button>
              <b-button
                size="sm"
                class="float-right mr-2 content-btn-cancel"
                @click="close()"
              >
                Cancelar
              </b-button>
            </div>
          </template>
        </b-modal>
      </div>
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
        slidesToShow: 3,
        slidesToScroll: 3,
        initialSlide:0,
        responsive: [
          {
            breakpoint: 1024,
            settings: {
              slidesToShow: 2,
              slidesToScroll: 2,
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
        { id: 1, url: require('@/assets/images/servicios/servicios_1.jpg'), title: 'VENTAS DE ASCENSORES',
          description:"Nuestro personal está capacitado para realizar las instalaciones mecánicas y electrónicas hasta que su equipo quede funcionando y cumpliendo rigurosamente los estándares de seguridad y calidad."
        },
        { id: 2, url: require('@/assets/images/servicios/servicios_2.jpg'), title: 'INSTALACIÓN',
          description:"Nuestro personal está capacitado para realizar las instalaciones mecánicas y electrónicas hasta que su equipo quede funcionando y cumpliendo rigurosamente los estándares de seguridad y calidad."
        },
        { id: 3, url: require('@/assets/images/servicios/servicios_3.jpg'), title: 'MANTENIMIENTO',
          description:"Ejecutamos mensualmente mantenimientos preventivos con técnicos especializados, cumpliendo con los estándares de calidad realizamos la inspección personalizada de todos los sistemas de seguridad y verificación de cada componente electrónico y mecánico, maximizando la vida útil del ascensor y evitando interrupciones para así lograr el óptimo funcionamiento del mismo."
        },
        { id: 4, url: require('@/assets/images/servicios/servicios_4.jpg'), title: 'EMERGENCIA',
          description:"Nuestros técnicos están constantemente capacitados y acuden con rapidez cuando reciben un aviso de emergencia y resuelven cualquier incidente eficazmente para que su ascensor vuelva a funcionar óptimamente lo antes posible."
        },
        { id: 5, url: require('@/assets/images/servicios/servicios_5.jpg'), title: 'REPARACIONES',
          description:"Contamos con personal capacitado para identificar fallas y averías, en la cual cumpliendo los estándares de calidad, podemos determinar y brindar una solución acertada a las paralizaciones que puede presentar el equipo, para ellos contamos con stock de repuestos originales y herramientas adecuadas para garantizar un correcto funcionamiento."
        },
        { id: 6, url: require('@/assets/images/servicios/servicios_6.jpg'), title: 'MODERNIZACIÓN',
          description:"Modernizamos la tecnología de su ascensor mejorando el confort y aumentando la seguridad del equipo, debido al desgaste de algunas tecnologías y componentes que conllevan a la modernización de un ascensor, los cuales nos llevan a ofrecer un amplio abanico de modernizaciones y mejores estándares tecnológicos. (Web) "
        },
      ],
      show: false,
    }
  },
}
</script>
<style>
.content_servicios {
  padding: 120px 0;
  background: #e3e8ee;
}
.content-title-section {
  font-size: 70px;
  padding-top: 20px;
  margin-bottom: 50px;
  color: #445b69;
  text-transform: uppercase;
}
.content_img {
    height: 250px !important;
    width: 100%;
}
.content-modal_image {
  width: 75%;
  height: 300px;
}
.content-img_title {
    font-size: 23px;
    font-weight: bold;
    color:#445b69;
    font-family: 'MyriadPro-Regular';
}
.modal-header {
  color: white;
  background-color: #4d8683 !important;
}
.close {
  color: white !important;
}
.content-btn {
  font-size: 20px !important;
  border-radius: 10px !important;
  cursor: pointer !important;
}
.content-btn-cancel {
  background: white !important;
  color: black !important;
  font-size: 20px !important;
  border-radius: 10px !important;
  cursor: pointer !important;
}
.content-btn_card {
  color: white;
  background: #4d8683 !important;
  font-size: 25px;
  cursor: pointer !important;
}
.content-modal_icon {
  height: 25px;
  width: 25px;
}
@media (max-width: 768px) {
  .content-modal_image {
    width: 75%;
    height: 150px;
  }
  h2 {
    font-size: 42px !important;
    align-items: center !important;
    font-weight: bold !important;
  }
}
</style>
