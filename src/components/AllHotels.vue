<template>
  <div class="product-box" id="allhotels">
    <div class="section notopmargin notopborder" id="section">
      <div class="container clearfix">
        <div class="heading-block center nomargin">
          <h3>Hotels</h3>
        </div>
      </div>
    </div>
    <div class="shop grid-container clearfix" id="shop">
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
#section {
  margin: 0;
}
#allhotels {
  padding-bottom: 5%;
}
</style>
