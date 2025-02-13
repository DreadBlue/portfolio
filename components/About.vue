<template>
  <v-container fluid class="pa-3 h-screen bg-main" id="aboutme">
    <v-row style="margin-left: 90px; margin-right: 90px; padding-top: 200px;">
      <v-col cols="3" class="d-flex align-center">
        <div>
          <img
            class="w-100 position-relative bottom-0 left-0"
            src="/profile.png"
            alt="Foto personal"
            style="
              -webkit-mask-image: radial-gradient(
                circle,
                rgba(0, 0, 0, 1) 50%,
                rgba(0, 0, 0, 0) 100%
              );
              mask-image: radial-gradient(
                circle,
                rgba(0, 0, 0, 1) 50%,
                rgba(0, 0, 0, 0) 100%
              );
            "
          />
        </div>
      </v-col>
      <v-col cols="9" class="d-flex flex-column justify-center px-15">
        <p class="font-orbitron color-main text-h1">ABOUT ME</p>
        <p class="color-second font-montserrat text-h6">¡Hi!</p>
        <p class="color-second font-montserrat text-h6">Here, Cristian.</p>
        <p class="color-second font-montserrat mr-15">
          Involved in tech since a child and passionated by social science as
          well. Academy was an inside discussion where both sides won and
          finished with a literature bachelor with full stack web develpment
          master (in progress.) Three years working as freelancer focus on
          tourism field and web apps able to improve the results through web
          apps power.
        </p>
        <div class="d-flex ga-5 py-5">
          <v-btn>
            <svg-cv />
            <p>Curriculum</p>
          </v-btn>
          <v-btn>
            <svg-linkedin />
            <p>Linkedin</p>
          </v-btn>
          <v-btn>
            <svg-gmail />
            <p>Correo</p>
          </v-btn>
        </div>
      </v-col>
    </v-row>
    <v-row>
        <v-col cols="3">
            <p class="color-main">EDUCATION</p>
        </v-col>
        <v-col cols="9">

        </v-col>
    </v-row>
  </v-container>
</template>
