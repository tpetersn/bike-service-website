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
  <BNavbar v-b-color-mode="'dark'" :toggleable="true" variant="primary">
    <BNavbarBrand href="#">Menu</BNavbarBrand>
    <BNavbarToggle target="nav-offcanvas" />
    <BOffcanvas id="nav-offcanvas" title="Menu" placement="end" is-nav>
      <BNavbarNav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/book">Book</RouterLink>
        <BNavItem href="#">Service &amp; Pricing</BNavItem>
        <BNavItem href="#">Book An Appointment</BNavItem>
        <BNavItem href="#">About Us</BNavItem>
        <BNavItem href="#">Contact Us</BNavItem>
        <BNavItem href="#">Shop Hours</BNavItem>
      </BNavbarNav>
    </BOffcanvas>
  </BNavbar>

  <header>
    <div class="header-banner">
      <BImg src="/images/bike-rider-1.png" alt="Responsive image" class="img-fluid header-pic"/>

    </div>
    
    
  </header>
  <RouterView />
  <FooterBar></FooterBar>
</template>

<style lang="css">

</style>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.header-banner {
  width: 100%;
  overflow: hidden;
}


.header-pic{
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
