<template>
  <button @click="active = !active">Toggle lightbox</button>
  <vue-wrapping-lightbox ref="lightbox">
    <img src="https://randomfox.ca/images/57.jpg" alt="" />
    <img src="https://randomfox.ca/images/117.jpg" alt="" />
    <img src="https://randomfox.ca/images/40.jpg" alt="" />
  </vue-wrapping-lightbox>
  <div class="images">
    <img
      src="https://randomfox.ca/images/57.jpg"
      alt=""
      @click="$refs.lightbox.openImage(0)"
      class="image"
    />
    <img
      src="https://randomfox.ca/images/117.jpg"
      alt=""
      @click="$refs.lightbox.openImage(1)"
      class="image"
    />
    <img
      src="https://randomfox.ca/images/40.jpg"
      alt=""
      @click="$refs.lightbox.openImage(2)"
      class="image"
    />
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";
import VueWrappingLightbox from "./VueWrappingLightbox.vue";

const active = ref(false);
</script>

<style>
.images {
  display: flex;
  gap: 10px;
}
.image {
  width: 100px;
  height: 100px;
  object-fit: cover;
}
</style>
