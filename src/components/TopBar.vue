<script setup>
import { onMounted, onUnmounted, ref } from "vue";

let isTopBarAnimated = ref(false);

const handleScroll = () => {
  const winOffset = window.scrollY || window.pageYOffset;

  if (winOffset >= 100) {
    isTopBarAnimated = true;
  } else {
    isTopBarAnimated = false;
  }
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>

<template>
  <div class="grax_tm_topbar opened">
    <div class="container">
      <div class="topbar_inner">
        <div class="logo">
          <a class="dark" href="#">
            <img src="../../public/img/logo/dark.png" alt="" />
          </a>
          <a class="light" href="#">
            <img src="../../public/img/logo/logo.png" alt="" />
          </a>
        </div>
        <div class="menu">
          <ul class="anchor_nav">
            <li class="current"><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#portfolio">Portfolio</a></li>
            <!-- <li><a href="#news">News</a></li> -->
            <li><a href="#contact">Contact</a></li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
