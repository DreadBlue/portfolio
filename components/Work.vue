<template>
  <v-container fluid class="px-3 py-15 bg-main">
    <v-row class="bg-mygrey rounded-t-lg mx-15">
      <v-col cols="12" class="d-flex justify-center align-center">
        <projectt class="pt-15" />
        <p class="font-orbitron text-h1 color-third pt-15 pb-0">
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
    <v-row class="bg-mygrey rounded-b-lg mx-15 py-10">
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
            <htmlsvg style="width: 31%" />
            <p>HTML5</p>
          </div>
          <div class="d-flex align-center ga-1">
            <csssvg style="width: 35%" />
            <p>CSS</p>
          </div>
          <div class="d-flex align-center ga-1">
            <sassvg style="width: 35%" />
            <p>SCSS</p>
          </div>
          <div class="d-flex align-center ga-1">
            <vue style="width: 35%" />
            <p>Vue JS</p>
          </div>
          <div class="d-flex align-center ga-1">
            <vuetify style="width: 32%" />
            <p>Vuetify</p>
          </div>
          <div class="d-flex align-center ga-1">
            <nuxt style="width: 35%" />
            <p>Nuxt</p>
          </div>
          <div class="d-flex align-center ga-1">
            <firebase style="width: 35%" />
            <p>Firebase</p>
          </div>
          <div class="d-flex align-center ga-1">
            <cloud style="width: 25%" />
            <p>Google Cloud</p>
          </div>
        </div>
      </v-col>
      <v-col cols="12" class="d-flex px-15 mx-3 ga-10 align-center">
        <div>
          <p class="text-h6 color-main pl-10">INTERMEDIATE</p>
        </div>
        <div class="d-flex">
            <div class="d-flex align-center ga-1">
              <react style="width: 40%" />
              <p>React</p>
            </div>
          <div class="d-flex align-center ga-1">
            <git style="width: 45%" />
            <p>Git</p>
          </div>
          <div class="d-flex align-center ga-1">
            <postgre style="width: 30%" />
            <p>Postgre</p>
          </div>
        </div>
      </v-col>
      <v-col cols="12" class="d-flex px-15 mx-3 ga-10 align-center">
        <div>
          <p class="text-h6 color-main pl-10">BASIC</p>
        </div>
        <div class="d-flex">
            <div class="d-flex align-center ga-1">
              <pythonsvg style="width: 32%" />
              <p>Python</p>
            </div>
          <div class="d-flex align-center ga-1">
            <django style="width: 32%" />
            <p>Django</p>
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
      "Web app developed for an extreme activities operator in Colombia, focus on the SEO and future expansion to new customers from different countries with different langua",
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
