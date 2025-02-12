<script setup>
import { ref } from "vue";

const projects = [
  {
    img: "/img/portfolio/tcuny.jpg",
    title: "Educational Resillience",
    type: "Web Development",
    link: "https://www.tcuny.com/",
    view: 1,
  },
  {
    img: "/img/portfolio/fitacademy.jpg",
    title: "FitAcademy",
    type: "Web Development",
    link: "https://www.fitacademy.id/",
    view: 1,
  },
  {
    img: "/img/portfolio/padangbaru.jpg",
    title: "Wesite Desa Padang Baru",
    type: "Web Development",
    link: "https://www.desa-padangbaru.vercel.app/",
    view: 1,
  },
  {
    img: "/img/portfolio/ruangtemu.png",
    title: "Ruang Temu Apps",
    type: "UI/UX Design",
    view: 2,
  },
  {
    img: "/img/portfolio/quiz.png",
    title: "Quiz App",
    type: "UI/UX Design",
    view: 2,
  },
  {
    img: "/img/portfolio/katar.png",
    title: "Logo Karang Taruna Desa Padang Baru",
    type: "Logo Design",
    view: 2,
  },
];

// console.log(projects);
</script>

<template>
  <div class="grax_tm_section" id="portfolio">
    <div class="grax_tm_portfolio">
      <div class="container">
        <div class="grax_tm_title_holder">
          <h3>Selected <span>Works</span></h3>
        </div>
        <div class="portfolio_list">
          <ul class="gallery_zoom my_waypoint">
            <li
              v-for="(project, index) in projects"
              :key="index"
              class="wow fadeInLeft"
              data-wow-duration="1.5s"
            >
              <div class="list_inner">
                <div class="image">
                  <img src="../../public/img/placeholders/1-1.jpg" alt="" />
                  <div
                    class="main"
                    :style="{ backgroundImage: `url(${project.img})` }"
                  ></div>
                </div>
                <div class="overlay"></div>
                <div class="details">
                  <h3>{{ project.title }}</h3>
                  <span>{{ project.type }}</span>
                </div>
                <div v-if="project.view === 1">
                  <a
                    class="grax_tm_full_link"
                    :href="project?.link"
                    target="_blank"
                    rel="noopener noreferrer"
                  >
                  </a>
                </div>

                <div v-if="project.view === 2">
                  <a class="grax_tm_full_link zoom" :href="project.img"> </a>
                </div>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
