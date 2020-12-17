<template>
  <div>
    <b-navbar class="navbar" toggleable="lg" type="dark" fixed="top">
      <div class="container">
        <b-navbar-brand href="#">
          <img
            :src="require('@/assets/images/Inicio/logo-white.png')"
            class="logo-brand"
            alt="logo"
          />
        </b-navbar-brand>

        <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

        <b-collapse is-nav id="nav_collapse">
          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
            <!-- Using button-content slot -->
            <b-nav-item
              class="nav-link"
              v-for="(link, index) in navLinks"
              :key="index"
              @click="nav(link)"
            >
              {{link.text}}
            </b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </div>
    </b-navbar>
  </div>
</template>

<script>
export default {
  data() {
    return {
      navLinks: [
        {
          text: "Inicio",
          id: "inicio",
        },
        {
          text: "Nosotros",
          id: "nosotros",
        },
        {
          text: "Servicios",
          id: "service",
        },
        {
          text: "Productos",
          id: "products",
        },
        {
          text: "Contáctenos",
          id: "contacto",
        },

      ],
    };
  },
  methods: {
    nav(link) {
      const position = document.getElementById(link.id).offsetTop;
      // smooth scroll
      window.scrollTo({ top: position, behavior: "smooth" });
    },
  },
};
</script>
<style>
/*NAVBAR*/
.logo-brand {
  max-width: 180px;
  min-width: 160px;
}
.navbar {
  text-transform: uppercase;
  font-weight: 700;
  font-size: 0.9rem;
  min-height: 100px;
  letter-spacing: 0.1rem;
  background: rgba(77, 134, 131, 1) !important;
}
.navbar-nav li {
  padding-right: 0.7rem;
}
.nav-link {
  color: white !important;
}
.nav-link:hover {
  color: #17ccb1 !important;
}
@media (max-width: 768px) {
  .navbar-nav {
    line-height: 50px;
  }
}
</style>
