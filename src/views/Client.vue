<template>
  <div class="client">
    <div v-for="images in slides" :key="images" :class="slide.class">
      <vueper-slides :bullets="false" :arrows="false" autoplay>
        <vueper-slide :image="slide.image" />
      </vueper-slides>
    </div>
  </div>
</template>
<script>
import { VueperSlides, VueperSlide } from "vueperslides";
import "vueperslides/dist/vueperslides.css";
import { mapState } from "vuex";
export default {
  data() {
    return {
      autoPlaying: true,
    };
  },
  components: { VueperSlides, VueperSlide },
  computed: {
    ...mapState("client", ["slides"]),
  },
};
</script>
<style scoped></style>
