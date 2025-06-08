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
</script>

<template>
  <BNavbar v-b-color-mode="'dark'" :toggleable="true" variant="primary">
    <BNavbarBrand href="#">Menu</BNavbarBrand>
    <BNavbarToggle target="nav-offcanvas" />
    <BOffcanvas id="nav-offcanvas" title="Menu" placement="end" is-nav>
      <BNavbarNav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <BNavItem href="#">Service &amp; Pricing</BNavItem>
        <BNavItem href="#">Book An Appointment</BNavItem>
        <BNavItem href="#">About Us</BNavItem>
        <BNavItem href="#">Contact Us</BNavItem>
        <BNavItem href="#">Shop Hours</BNavItem>
      </BNavbarNav>
    </BOffcanvas>
  </BNavbar>

  <header>
    <BImg src="https://picsum.photos/1280/400/?image=42" fluid alt="Responsive image" />
  </header>
  <RouterView />
</template>

<style lang="css">

</style>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}



@media (min-width: 1024px) {

}
</style>
