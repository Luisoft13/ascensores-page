<template>
  <section id="productos" class="content-section-products">
      <div class="container">
        <div class="content-center">
          <h2 class="content-productos_title">NUESTROS PRODUCTOS</h2>
          <div class="row">
            <div class="col-md-4">
                <div class="products_item">
                  <img :src="require('@/assets/images/productos/producto-1.jpg')" class="img-fluid rounded products_img">
                  <div class="products_hover">
                    <h3 class="products_title">ASCENSOR DE PASAJEROS</h3>
                    <i class="fas fa-suitcase products_icon"></i>
                  </div>
                </div>
            </div>
            <div class="col-md-4">
                <div class="products_item">
                  <img :src="require('@/assets/images/productos/producto-2.jpg')" class="img-fluid rounded products_img">
                  <div class="products_hover">
                    <h3 class="products_title">ASCENSOR MONTACAMILLA</h3>
                    <i class="fas fa-suitcase products_icon"></i>
                  </div>
                </div>
            </div>
            <div class="col-md-4 pb-10">
                <div class="products_item">
                  <img :src="require('@/assets/images/productos/producto-3.jpg')" class="img-fluid rounded products_img">
                  <div class="products_hover">
                    <h3 class="products_title">ASCENSOR MONTACARGA</h3>
                    <i class="fas fa-suitcase products_icon"></i>
                  </div>
                </div>
            </div>
            <div class="col-md-4 pb-10">
                <div class="products_item">
                  <img :src="require('@/assets/images/productos/producto-4.jpg')" class="img-fluid rounded products_img">
                  <div class="products_hover">
                    <h3 class="products_title">ASCENSOR MONTAVEHÍCULO</h3>
                    <i class="fas fa-suitcase products_icon"></i>
                  </div>
                </div>
            </div>
            <div class="col-md-4 pb-10">
                <div class="products_item">
                  <img :src="require('@/assets/images/productos/producto-5.jpg')" class="img-fluid rounded products_img">
                  <div class="products_hover">
                    <h3 class="products_title">ASCENSOR DE MINUSVÁLIDOS</h3>
                    <i class="fas fa-suitcase products_icon"></i>
                  </div>
                </div>
            </div>
            <div class="col-md-4 pb-10">
                <div class="products_item">
                  <img :src="require('@/assets/images/productos/producto-6.jpg')" class="img-fluid rounded products_img">
                  <div class="products_hover">
                    <h3 class="products_title">TABLEROS DE CONTROL O CUADRO DE MANIOBRA</h3>
                    <i class="fas fa-suitcase products_icon"></i>
                  </div>
                </div>
            </div>
          </div>
        </div>
      </div>
    </section>
</template>
<style>
.content-section-products {
    padding-top: 120px;
}
.content-productos_title {
    font-size: 70px;
    color:#445b69;
    font-family: 'MyriadPro-Regular';
    padding-top: 20px;
    margin-bottom: 50px;
}
.products_item {
    position: relative;
    width: 100%;
    height: 100%;
    overflow: hidden;
    padding-bottom: 60px !important;
}
.products_hover {
    position: absolute;
    background:rgba(77, 134, 131, 0.7)!important;
    top:0;
    left: 0;
    width: 100%;
    height: 83%;
    color: var(--white-color);
    text-align: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
    transform: translateX(100%);
    cursor: pointer;
    transition: transform .3s ease-in-out;
}
.products_item:hover .products_hover {
    transform: translateX(0%);
}
.products_icon {
    margin-top: 10px;
    font-size: 30px;
}
</style>
