<template>
  <div class="product-box">
    <vueper-slides
      :bullets="true"
      autoplay
      class="no-shadow"
      :visible-slides="3"
      slide-multiple
      :gap="3"
      :slide-ratio="1 / 4"
      :dragging-distance="200"
      :breakpoints="{ 800: { visibleSlides: 2, slideMultiple: 2 } }"
    >
    
      <vueper-slide
        v-for="i in slidertwo"
        :key="i"
        :title="i.h1"
        :image="i.img1"
      />
    </vueper-slides>
  </div>
</template>

<script>
import { VueperSlides, VueperSlide } from "vueperslides";
import "vueperslides/dist/vueperslides.css";
import { mapState } from "vuex";
export default {
  computed: {
    ...mapState("slider", ["slidertwo"]),
  },
  components: { VueperSlides, VueperSlide },
};
</script>
<style scoped>
vueper-slide {
  background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
}
.vueperslides--fixed-height {
  height: 85vh;
  width: 100%;
}
.vueperslides__arrow {
  background-color: #e21111;
  z-index: 10;
}
</style>
