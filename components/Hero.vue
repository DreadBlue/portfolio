<template>
  <v-container fluid class="pa-3">
    <v-row class="bg-main h-screen d-flex align-center px-15">
      <v-col cols="6" class="text-main" style="z-index: 1">
        <div class=" pl-7">
          <div class="d-flex font-exo text-subtitle mb-10">
            <p class="color-main"><</p>
            <p class="mx-2">Cristian Prada</p>
            <p class="color-main">/></p>
          </div>
          <p class="font-orbitron text-h1">Full</p>
          <p class="font-orbitron text-h1">Stack</p>
          <p class="font-orbitron text-h1">Developer</p>
          <p class="mt-5 font-monserrat">
            Building scalable, dynamic and high performance web applications
            with cloud solutions that help businesses grow and innovate.
          </p>
        </div>
      </v-col>
      <v-col
        cols="6"
        class="text-main d-flex flex-column align-end justify-center pr-15 ga-5"
        style="height: 100%; z-index: 0"
      >
        <img
          class="position-absolute right-0"
          style="
            width: 23%;
            opacity: 70%;
            z-index: 0;
            margin-right: 24%;
            filter: drop-shadow(0 0 30px rgba(0, 153, 255, 0.8));
          "
          src="/public/hero.png"
          alt="Fondo"
        />
        <div class="d-flex flex-column ga-5" style="z-index: 1">
          <v-hover v-slot:default="{ isHovering, props }">
            <NuxtLink
              class="text-subtitle-1 font-exo text-decoration-none text-main"
              v-bind="props"
              to="/about"
              >MY WORK</NuxtLink
            >
            <NuxtLink
              class="text-subtitle-1 font-exo text-decoration-none text-main"
              v-bind="props"
              to="/about"
              >ABOUT ME</NuxtLink
            >
            <!-- <NuxtLink
              class="text-subtitle-1 font-exo text-decoration-none"
              :class="isHovering ? 'color-main' : 'text-main'"
              v-bind="props"
              to="/about"
              >LINKS</NuxtLink
            > -->
          </v-hover>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>
