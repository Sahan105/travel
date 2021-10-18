<template>
  <div class="product-box" id="featured-hotel">
    <div class="section notopmargin notopborder">
      <div class="container clearfix">
        <div class="heading-block center nomargin">
          <h3>Featured Hotels</h3>
        </div>
      </div>
    </div>
    <div id="shop" class="shop grid-container clearfix">
      <div
        class="product clearfix"
        v-for="hotel in hotels"
        :key="hotel"
        id="product"
      >
        <HotelCart :hotel="hotel" />
      </div>
    </div>
  </div>
</template>
<script>
import { mapState } from "vuex";
import HotelCart from "../components/carts/HotelCart";
export default {
  name: "productbox",
  computed: {
    ...mapState("productbox", ["hotels"]),
  },
  components: {
    HotelCart,
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
#featured-hotel {
  padding-bottom: 5%;
}
</style>
