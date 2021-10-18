<template>
  <div class="product-box" id="allticket">
    <div class="section notopmargin notopborder" id="section">
      <div class="container clearfix">
        <div class="heading-block center nomargin">
          <h3>Tickets</h3>
        </div>
      </div>
    </div>
    <div class="shop grid-container clearfix" id="shop">
      <div
        class="product clearfix"
        v-for="ticket in tickets"
        :key="ticket"
        id="product"
      >
        <TicketCart :ticket="ticket" />
      </div>
    </div>
  </div>
</template>

<script>
import TicketCart from "../components/carts/TicketCart";
import { mapState } from "vuex";
export default {
  computed: {
    ...mapState("productbox", ["tickets"]),
  },
  components: {
    TicketCart,
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
#allticket {
  padding-bottom: 5%;
}
</style>
