<template>
  <v-container>
    <v-row>
      <v-col cols="6">
        <p class="font-exo text-h3 color-main">{{ item.title }}</p>
        <p class="mr-12 py-5 font-monserrat">
          {{ item.description }}
        </p>
        <div class="d-flex py-5 ga-5">
          <svg-js v-if="item.js" />
          <svg-react v-if="item.react" />
          <svg-nuxt v-if="item.nuxt" />
          <svg-firebase v-if="item.firebase" />
          <svg-cloud v-if="item.cloud" />
          <svg-vuetify v-if="item.vuetify" />
          <svg-git v-if="item.git" />
        </div>
          <NuxtLink to="`https://${{item.link}}`" class="text-decoration-none color-third font-exo d-flex align-center ga-2" style="font-size: 1.2rem;"> 
            <svg-link/>
            {{ item.link }}
          </NuxtLink>
      </v-col>
      <v-col cols="6">
        <div class=" elevation-15 rounded-lg">
          <img
            class="w-100 rounded-lg"
            :src="images[0]"
            alt="Project screen"
            @click="handleModal(item.title)"
          />
        </div>
        <div class="d-flex justify-space-evenly pt-15">
          <div class="w-25 elevation-15 rounded-lg" @click="imageSelector(1)">
            <img
              class="w-100 rounded-lg"
              :src="images[1]"
              alt="Abya Yala web"
            />
          </div>
          <div class="w-25 elevation-15 rounded-lg" @click="imageSelector(2)">
            <img
              class="w-100 rounded-lg"
              :src="images[2]"
              alt="Abya Yala web"
            />
          </div>
          <div class="w-25 elevation-15 rounded-lg" @click="imageSelector(3)">
            <img
              class="w-100 rounded-lg"
              :src="images[3]"
              alt="Abya Yala web"
            />
          </div>
        </div>
      </v-col>
    </v-row>
    <modal v-if="showModal && item.title == idModal" :modalImages="images" />
  </v-container>
</template>

<script setup>
import { useGeneralStore } from "/stores/general.js";

const useGeneral = useGeneralStore();
const showModal = computed(() => useGeneral.showModal);
const idModal = computed(() => useGeneral.idModal);

const props = defineProps({
  item: {
    type: Object,
  },
});

const images = ref([
  props.item.img,
  props.item.img2,
  props.item.img3,
  props.item.img4,
]);

function imageSelector(image) {
  const item = images.value.splice(image, 1)[0];
  images.value.unshift(item);
}

function handleModal() {
  useGeneral.updateDetails({ showModal: true });
  useGeneral.updateDetails({ idModal: props.item.title });
}
</script>
