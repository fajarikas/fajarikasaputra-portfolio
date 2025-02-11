<script setup>
import { onMounted, ref } from "vue";

const userName = ref("Fajar Ika Saputra");
const userJob = ref("A Curious Web Developer & UI/UX Designer");

onMounted(() => {
  // Fungsi untuk memproses efek animasi
  const applyAnimation = (selector) => {
    let element = $(selector); // Ambil elemen berdasarkan selector
    let start = '<span class="word">';
    let char = '<span class="character">';
    let end = "</span>";
    let space = "&nbsp;";
    let allHTML = "";

    // Proses teks untuk animasi
    $.each(element.text().split(" "), function (i, e) {
      if (i !== 0) {
        allHTML += char + space + end;
      }
      allHTML += start;
      $.each(e.split(""), function (ii, ee) {
        allHTML += char + ee + end;
      });
      allHTML += end;
    });

    element.html(allHTML).addClass("ready");

    // Tambahkan class 'opened' setelah timeout
    setTimeout(() => {
      document
        .querySelectorAll(`${selector} .character`)
        .forEach((charElement) => {
          charElement.classList.add("opened");
        });
    }, 500); // Sesuaikan timeout jika diperlukan
  };

  // Terapkan efek animasi pada userName dan userJob
  applyAnimation(".fn_animation.name"); // Untuk userName
  applyAnimation(".fn_animation.job"); // Untuk userJob

  // Tambahkan class 'opened' ke elemen lainnya
  setTimeout(() => {
    jQuery(".grax_tm_topbar").addClass("opened");
    jQuery(".grax_tm_down").addClass("opened");
  }, 500);
});
</script>

<template>
  <div class="grax_tm_hero" id="home">
    <div class="bg">
      <div
        class="image"
        data-img-url="../public/img/slider/background.png"
      ></div>
      <div class="overlay"></div>
    </div>
    <div class="content">
      <div class="container">
        <div class="details" data-animation="toTop">
          <!-- Animation Values: toTop, toRight, scale, rotate -->
          <h3 class="fn_animation name"> {{ userName }}</h3>
          <span class="fn_animation job ready">{{ userJob }}</span>
        </div>
        <div class="flex items-center justify-center h-screen">
          <img
            class="w-full h-auto lg:w-[50%] fixed right-0"
            src="../../public/img/slider/profile.png"
          />
        </div>

        <div class="grax_tm_down" data-skin="light">
          <div class="line_wrapper">
            <div class="line"> </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Tambahkan gaya CSS Anda di sini */
</style>
