<template>
<section class="content-section_contact">
  <div class="container">
    <form @submit.prevent="sendEmail">
      <div class="row">
        <div class="col-md-6 mt-4">
          <div class="row">
            <div class="col-md-12 text-center">
              <p class="content-title_contact">OBTEN TU COTIZACIÓN</p>
            </div>
            <div class="col-md-6">
              <div class="form-group">
                <input
                  type="text"
                  class="form-control"
                  v-model="name"
                  name="name"
                  required
                  placeholder="Nombre"
                />
              </div>
            </div>
            <div class="col-md-6">
              <div class="form-group">
                <input
                  type="text"
                  class="form-control"
                  v-model="lastname"
                  name="lastname"
                  placeholder="Apellidos"
                />
              </div>
            </div>
            <div class="col-md-12">
              <div class="form-group">
                <input
                  type="email"
                  class="form-control"
                  required
                  :rules="rules.email"
                  v-model="email"
                  name="email"
                  placeholder="Email"
                />
              </div>
            </div>
            <div class="col-md-12">
              <div class="form-group">
                <input
                  type="text"
                  class="form-control"
                  required
                  v-model="company"
                  name="company"
                  placeholder="Empresa"
                />
              </div>
            </div>
            <div class="col-md-12">
              <div class="form-group">
                <input
                  type="number"
                  class="form-control"
                  v-model="phone"
                  name="phone"
                  placeholder="Teléfono (optional)"
                />
              </div>
            </div>
            <div class="col-md-12">
              <div class="form-group">
                <input
                  type="text"
                  class="form-control"
                  v-model="distrit"
                  name="distrit"
                  placeholder="Distrito"
                />
              </div>
            </div>
            <div class="col-md-12">
              <div class="form-group">
                <textarea
                  class="form-control"
                  id="exampleFormControlTextarea1"
                  rows="3"
                  min="5"
                  v-model="message"
                  name="message"
                  placeholder="Mensaje"
                ></textarea>
              </div>
            </div>
            <div class="col-md-12">
              <input type="submit" class="btn content-btn-send full-width" value="Enviar"/>
            </div>
          </div>
        </div>
        <div class="col-md-6 mt-4">
          <img class="contact-image" :src="require('@/assets/images/contact/contacto_img.png')" alt="">
        </div>
      </div>
    </form>
  </div>
</section>
</template>
<script>
import emailjs from "emailjs-com";
import EMAIL_VALID_REGEX from '@/components/form/regex.js'

export default {
  data() {
    return {
      submitted: false,
      name: "",
      email: "",
      message: "",
      distrit:"",
      phone:"",
      lastname:"",
      company:"",
      rules: {
        email: [
          (v) => !!v || 'El campo email es requerido',
          (v) =>
            EMAIL_VALID_REGEX.test(v) ||
            'El campo email no es válido'
        ]
      }
    };
  },
  methods: {
    sendEmail(e) {
      const SERVICE_ID = "service_9jjb6gq";
      const USER_ID = "user_0q5uzp2eg9jDuDBAeYM6h";
      const TEMPLATE_ID = "template_9vqaajh";

      try {
        const response = emailjs.sendForm(
          SERVICE_ID,
          TEMPLATE_ID,
          e.target,
          USER_ID,
          {
            name: this.name,
            lastname:this.lastname,
            email: this.email,
            phone:this.phone,
            distrit:this.distrit,
            company:this.company,
            message: this.message,

          },
          this.submitted =true,
        );
        console.log(response);
      } catch (error) {
        console.log({ error });
      }
      // Reset form field
      this.name = "";
      this.lastname=""
      this.email = "";
      this.company ="";
      this.phone="",
      this.distrit="",
      this.message = "";
    },
  },
};
</script>
<style scoped>
.content-section_contact { padding: 120px 0; }
.content-title_contact {
  color:#445b69;
  font-size:34px;
  font-weight: bold;
}
.content-btn-send {
  background-color: rgba(77, 134, 131, 1);
  color: white;
  font-size: 18px;
  width: 100%;
}
.form-group {
  font-size: 17px;
  color:#445b69;
  font-size:34px;
}
.correcto {
  background-color: green;
  color:white;
  padding: 15px;
}
.contact-image {
  width: 100%;
  height: 100%;
  padding-bottom: 200px !important;
}
@media (max-width: 768px) {
  .contact-image {
    display: none;
    padding-bottom: 200px !important;
  }
  h2 {font-size:50px !important; align-items: center !important;}
}
</style>
