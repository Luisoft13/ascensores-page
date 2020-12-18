<template>
  <!--NOSOTROS SECTION-->
  <section id="nosotros">
    <div class="container">
      <div>
        <div class="text-center">
          <img
            class="logo-section-nosotros"
            :src="require('@/assets/images/Nosotros/logo_pacific.png')"
            alt=""
          />
        </div>
        <p class="content-title text-center">
          "El único modo de hacer un gran trabajo es amar lo que haces"
        </p>
        <p class="content-subtitle text-center">
          Ascensores Pacific SAC es una empresa peruana, especializada en
          brindar servicios de instalación, mantenimiento, reparación,
          modernización y ventas de ascensores, priorizando la calidad del
          servicio
        </p>
        <div class="row content_first align-items-center">
          <div class="col-md-6 col-sm-12 content-img">
            <img
              class="content-img-mision"
              :src="require('@/assets/images/Nosotros/mision.jpg')"
              alt=""
            />
          </div>
          <div class="col-md-6 col-sm-12">
            <p
              class="content-title-vision-mision"
              style="text-transform: uppercase"
            >
              1.Misión
            </p>
            <p class="content-text-vision-mision">
              La misión principal de ASCENSORES PACIFIC y del equipo humano que
              lo conforma es garantizar la satisfacción de nuestros clientes así
              mismo otorgar seguridad y confianza con nuestro servicio a un
              precio competitivo.
            </p>
          </div>
        </div>
        <div class="row content_second align-items-center">
          <div class="col-md-6">
            <p
              class="content-title-vision-mision"
              style="text-transform: uppercase"
            >
              2.Visión
            </p>
            <p class="content-text-vision-mision">
              Ser líder de nuestro sector y el mejor referente en instalación,
              mantenimiento, reparación y modernización de ascensores ofreciendo
              altos estándares de calidad e innovación tecnológica a nivel
              nacional.
            </p>
          </div>
          <div class="col-md-6 content-img">
            <img
              class="content-img-mision"
              :src="require('@/assets/images/Nosotros/vision.jpg')"
              alt=""
            />
          </div>
        </div>
        <div class="mt-5">
          <b-button
            class="content-btn_brochure"
            size="lg"
            pill
            href="./brochure-ascensores-pacific-sac.pdf"
            target="_blank"
          >
            Ver Brochure
          </b-button>
        </div>
      </div>
    </div>
  </section>
</template>
<style>
section {
  padding: 120px 0;
}
.logo-section-nosotros {
  max-width: 360px;
  min-width: 320px;
}
.content_first {
  padding: 0 160px 60px 160px;
}
.content_second {
  padding: 0 160px 60px 160px;
}
.content-title {
  margin-top: 30px;
  font-size: 28px;
  color: #4d8683;
  text-transform: uppercase;
  font-weight: bold;
  padding: 0 200px 0 200px;
  font-family: "MyriadPro-Regular";
}
.content-subtitle {
  font-size: 24px;
  color: #211915;
  line-height: 1.5;
  padding: 0 150px 0 150px;
  font-family: "Roboto", sans-serif;
  padding-bottom: 50px;
}
.content-title-vision-mision {
  color: #445b69;
  font-size: 52px;
  line-height: 1.8;
  font-weight: bold;
  margin-bottom: 0px;
}
.content-text-vision-mision {
  font-family: "MyriadPro-Regular";
  font-size: 24px;
  color: #211915;
  line-height: 30px;
}
.content-img-mision {
  width: 100%;
  height: 100%;
}
.content-img {
  overflow: hidden;
}
.content-img img {
  transition: all 1.5s ease;
}
.content-img:hover img {
  transform: scale(1.5);
}
.content-btn_brochure {
  color: white;
  background: #4d8683 !important;
  font-size: 25px;
  cursor: pointer !important;
}
@media (max-width: 1024px) {
  .logo-section-nosotros {
    max-width: 260px;
    min-width: 200px;
  }
  .content-title {
    padding: 0px;
    font-size: 24px;
  }
  .content-subtitle {
    padding: 0px;
    font-size: 18px;
  }
  .content_first {
    padding: 0px;
    flex-wrap: wrap-reverse !important;
    text-align: center;
  }
  .content_second {
    padding: 0px;
    text-align: center;
  }
  .content-title-vision-mision {
    font-size: 44px;
  }
  .content-text-vision-mision {
    font-size: 18px;
  }
  .content-btn_brochure {
    font-size: 18px;
  }
}
</style>
