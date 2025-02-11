<script setup>
import About from "./components/About.vue";
import Contact from "./components/Contact.vue";
import Copyright from "./components/Copyright.vue";
import Cursor from "./components/Cursor.vue";
import Hero from "./components/Hero.vue";
import MobileMenu from "./components/MobileMenu.vue";
import ModalBox from "./components/ModalBox.vue";
import PageProgress from "./components/PageProgress.vue";
import Portfolio from "./components/Portfolio.vue";
import Preloader from "./components/Preloader.vue";
import Settings from "./components/Settings.vue";
import Skills from "./components/Skills.vue";
import Talk from "./components/Talk.vue";
import TopBar from "./components/TopBar.vue";
</script>

<template>
  <!-- <Preloader /> -->
  <div class="grax_tm_all_wrap" data-magic-cursor="" data-color="crimson">
    <Settings />
    <ModalBox />
    <TopBar />
    <MobileMenu />
    <Hero />
    <About />
    <Portfolio />
    <Skills />
    <Talk />
    <Contact />
    <Copyright />
    <Cursor />
    <PageProgress />
  </div>
</template>

<style scoped></style>
