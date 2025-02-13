<template>
  <v-container fluid class="px-3 bg-main" id="mywork">
    <v-row class="bg-mygrey rounded-t-lg" style="margin-left: 90px; margin-right: 90px; background-image: url('/wing5.png'); background-size: cover; background-blend-mode:overlay;">
      <v-col cols="12" class="d-flex justify-center align-center">
        <svg-projectt class="pt-15" />
        <p class="font-orbitron text-h2 color-third pt-15 pb-0">
          SIDE PROJECTS
        </p>
      </v-col>
      <v-col
        v-for="project in projects"
        cols="12"
        class="px-15 py-15"
        :key="project.title"
      >
        <Project :item="project" />
      </v-col>
    </v-row>
    <v-row class="bg-mygrey rounded-b-lg pb-10" style="margin-left: 90px; margin-right: 90px;">
      <v-col cols="12">
        <div class="d-flex ga-3 font-exo justify-space-between px-15 py-10" style="font-weight: 700;">
          <p>TECHNOLOGY STACK</p>
          <codesvg />
          <p>TECHNOLOGY STACK</p>
          <tech />
          <p>TECHNOLOGY STACK</p>
          <codesvg />
          <p>TECHNOLOGY STACK</p>
          <tech />
          <p>TECHNOLOGY STACK</p>
          <codesvg />
          <p>TECHNOLOGY STACK</p>
        </div>
      </v-col>
      <v-col cols="12" class="d-flex px-15 mx-3 ga-10 align-center">
        <div>
          <p class="text-h6 color-main pl-10">ADVANCED</p>
        </div>
        <div class="d-flex">
          <div class="d-flex align-center ga-1">
            <svg-htmlsvg style="width: 31%" />
            <p style="font-size: 0.8rem;">HTML5</p>
          </div>
          <div class="d-flex align-center ga-1">
            <svg-csssvg style="width: 35%" />
            <p style="font-size: 0.8rem;">CSS</p>
          </div>
          <div class="d-flex align-center ga-1">
            <svg-sassvg style="width: 35%" />
            <p style="font-size: 0.8rem;">SCSS</p>
          </div>
          <div class="d-flex align-center ga-1">
            <svg-vue style="width: 35%" />
            <p style="font-size: 0.8rem;">Vue JS</p>
          </div>
          <div class="d-flex align-center ga-1">
            <svg-vuetify style="width: 32%" />
            <p style="font-size: 0.8rem;">Vuetify</p>
          </div>
          <div class="d-flex align-center ga-1">
            <svg-nuxt style="width: 35%" />
            <p style="font-size: 0.8rem;">Nuxt</p>
          </div>
          <div class="d-flex align-center ga-1">
            <svg-firebase style="width: 35%" />
            <p style="font-size: 0.8rem;">Firebase</p>
          </div>
          <div class="d-flex align-center ga-1">
            <svg-cloud style="width: 25%" />
            <p style="font-size: 0.8rem;">Google Cloud</p>
          </div>
        </div>
      </v-col>
      <v-col cols="12" class="d-flex px-15 mx-3 ga-10 align-center">
        <div>
          <p class="text-h6 color-main pl-10">INTERMEDIATE</p>
        </div>
        <div class="d-flex">
            <div class="d-flex align-center ga-1">
              <svg-react style="width: 40%" />
              <p style="font-size: 0.8rem;">React</p>
            </div>
          <div class="d-flex align-center ga-1">
            <svg-git style="width: 45%" />
            <p style="font-size: 0.8rem;">Git</p>
          </div>
          <div class="d-flex align-center ga-1">
            <svg-postgre style="width: 30%" />
            <p style="font-size: 0.8rem;">Postgre</p>
          </div>
          <div class="d-flex align-center ga-1">
            <svg-mongo style="width: 30%" />
            <p style="font-size: 0.8rem;">MongoDB</p>
          </div>
        </div>
      </v-col>
      <v-col cols="12" class="d-flex px-15 mx-3 ga-10 align-center">
        <div>
          <p class="text-h6 color-main pl-10">BASIC</p>
        </div>
        <div class="d-flex">
            <div class="d-flex align-center ga-1">
              <svg-pythonsvg style="width: 32%" />
              <p style="font-size: 0.8rem;">Python</p>
            </div>
          <div class="d-flex align-center ga-1">
            <svg-django style="width: 32%" />
            <p style="font-size: 0.8rem;">Django</p>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
const projects = {
  abyayala: {
    title: "1. ABYA YALA HOSTEL",
    description:
      "Web app developed for a hostel, focus on improving the human resource involved in booking and customer management system. Hostel process automatized and manager space created for owner.",
    js: true,
    react: true,
    nuxt: true,
    firebase: true,
    cloud: true,
    vuetify: false,
    git: true,
    img: "/abya.png",
    img2: "/abya2.png",
    img3: "/abya3.png",
    img4: "/abya4.png",
    link: "www.abyayalahostel.com",
  },
  reservita: {
    title: "2. LA RESERVITA",
    description:
      "Web app developed for an extreme activities operator in Colombia, focus on the SEO and future expansion to new customers from different countries with different languages approaches.",
    js: true,
    react: false,
    nuxt: true,
    firebase: true,
    cloud: true,
    vuetify: true,
    git: true,
    img: "/reservita.png",
    img2: "/reservita2.png",
    img3: "/reservita3.png",
    img4: "/reservita4.png",
    link: "www.lareservita.com",
  },
};
</script>
