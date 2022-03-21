<template>
  <vue-wrapping-lightbox ref="lightbox" class="images">
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
  </vue-wrapping-lightbox>
</template>

<script lang="ts" setup>
import VueWrappingLightbox from "./VueWrappingLightbox.vue";
</script>

<style>
.images {
  display: grid;
  gap: 10px;
  grid-template-columns: repeat(3, 100px);
  grid-auto-rows: 100px;
}
.image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
