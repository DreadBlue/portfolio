<template>
  <div
    class="d-flex flex-column justify-center align-center overlay px-15"
    @click.self="useGeneral.updateDetails({ showModal: false })"
  >
    <div class="w-75 elevation-15 rounded-lg">
      <img
        class="w-100 rounded-lg"
        :src="images[0]"
        alt="Abya Yala web"
        @click="handleModal()"
      />
    </div>
    <div class="d-flex justify-space-evenly pt-5">
      <div class="elevation-15 rounded-lg" @click="imageSelector(1)" style="width: 20%;">
        <img class="w-100 rounded-lg" :src="images[1]" alt="Abya Yala web" />
      </div>
      <div class="elevation-15 rounded-lg" @click="imageSelector(2)" style="width: 20%;">
        <img class="w-100 rounded-lg" :src="images[2]" alt="Abya Yala web" />
      </div>
      <div class="elevation-15 rounded-lg" @click="imageSelector(3)" style="width: 20%;">
        <img class="w-100 rounded-lg" :src="images[3]" alt="Abya Yala web" />
      </div>
    </div>
  </div>
</template>

<script setup>
import { useGeneralStore } from "/stores/general.js";

const props = defineProps({
    modalImages: {
    type: Object,
  },
});

const images = ref(props.modalImages)
const useGeneral = useGeneralStore();

function imageSelector(image) {
  const item = images.value.splice(image, 1)[0];
  images.value.unshift(item);
}
</script>

<style scoped>
.overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background: rgba(0, 0, 0, 0.9); /* Oscuro con opacidad */
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 1000; /* Asegura que se sobreponga a todo */
}
</style>
