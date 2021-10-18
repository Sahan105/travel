<template>
  <div class="product-box" id="featured-event">
    <div class="section notopmargin notopborder" id="section">
      <div class="container clearfix">
        <div class="heading-block center nomargin">
          <h3>Featured Events</h3>
        </div>
      </div>
    </div>
    <div id="shop" class="shop grid-container clearfix">
      <div
        class="product clearfix"
        v-for="event in events"
        :key="event"
        id="product"
      >
        <EventCart :event="event" />
      </div>
    </div>
  </div>
</template>
<script>
import { VueperSlides, VueperSlide } from "vueperslides";
import "vueperslides/dist/vueperslides.css";
import { mapState } from "vuex";
import EventCart from "../components/carts/EventCart";
export default {
  name: "productbox",
  computed: {
    ...mapState("productbox", ["events"]),
  },
  components: {
    EventCart,
    VueperSlides,
    VueperSlide,
  },
};
</script>
<style scoped>
#shop {
  padding: 0 10%;
}
#product {
  padding: 0;
}
#section {
  margin: 0;
}
#featured-event {
  padding-bottom: 5%;
}
</style>
