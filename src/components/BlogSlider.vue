<template>
  <div>
    <vueper-slides :fixed-height="false" :bullets="true" fade autoplay>
      <vueper-slide
        v-for="slide in blogslider"
        :key="slide"
        :image="slide.image"
        :title="slide.title"
        :content="slide.content"
      />
    </vueper-slides>
  </div>
</template>

<script>
import { VueperSlides, VueperSlide } from "vueperslides";
import "vueperslides/dist/vueperslides.css";
import { mapState } from "vuex";
export default {
  name: "slider",
  computed: {
    ...mapState("slider", ["blogslider"]),
  },
  components: { VueperSlides, VueperSlide },
};
</script>
<style>
vueper-slide {
  background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
}
.vueperslides--fixed-height {
  height: 50vh;
}
.vueperslides__arrow {
  background-color: #464646;
}
</style>
