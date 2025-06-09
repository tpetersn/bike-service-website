<script setup>
import { RouterLink, RouterView } from 'vue-router'
import {
  BImg,
  BNavbar,
  BNavbarBrand,
  BNavbarNav,
  BNavbarToggle,
  BNavItem,
  BOffcanvas
} from "bootstrap-vue-next";
import FooterBar from "@/components/FooterBar.vue";
</script>

<template>
  <BNavbar :toggleable="true" variant="primary">
    <h4 class="navbar-brand">The Bike Doctor</h4>
    <BNavbarToggle target="nav-offcanvas" />
    <BOffcanvas id="nav-offcanvas" title="Menu" placement="end" is-nav>
      <BNavbarNav>
        <BNavItem to="/">Home</BNavItem>
        <BNavItem to="/book">Book An Appointment</BNavItem>
        <BNavItem href="#services">Service &amp; Pricing</BNavItem>
        <BNavItem href="/#tech">About Us</BNavItem>
        <BNavItem href="/#about">Contact Us</BNavItem>
        <BNavItem href="/#about">Shop Hours</BNavItem>
      </BNavbarNav>
    </BOffcanvas>
  </BNavbar>

  <header>
    <div class="header-banner">
      <BImg src="/bike-service-website/images/bike-rider-1.png" alt="Responsive image" class="img-fluid header-pic"/>

    </div>


  </header>
  <RouterView class="p-3" />
  <FooterBar id="about"></FooterBar>
</template>

<style lang="css">
/* Global styles go here */
</style>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}
h4 {
  font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  font-weight: thin;
  font-style: italic;
  font-size: 22px;
  padding-left: 10px;
}

.header-banner {
  margin-bottom:0px;
  padding-bottom:0px;
  width: 100%;
  overflow: hidden;
  
}


.header-pic{
  margin-bottom:0px;
  padding-bottom:0px;
  width: 100%;
  height: 225px;
  object-fit: cover;
  display: block;
  
}


@media (min-width: 1024px) {
  .header-pic {
    height: 400px;

  }

}

</style>
