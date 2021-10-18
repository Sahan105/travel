<template>
  <div class="product-box">
    <section id="content">
      <div class="content-wrap">
        <div class="container clearfix">
          <div
            id="shop"
            class="shop grid-container clearfix"
            data-layout="fitRows"
          >
            <div class="product clearfix" id="product">
              <div class="product-image" id="product-image">
                <a href="#"
                  ><img
                    style="height: 280px; width: 370px"
                    :src="ticket.img1"
                    alt="Checked Short Dress"
                /></a>
                <a href="#"
                  ><img
                    style="height: 280px; width: 370px"
                    :src="ticket.img2"
                    alt="Checked Short Dress"
                /></a>
                <div class="product-overlay">
                  <a href="#" class="add-to-cart"
                    ><i class="icon-shopping-cart"></i
                    ><span> Add to Cart</span></a
                  >
                </div>
              </div>
              <div id="text">
                <div class="product-title">
                  <h3>
                    <a href="#">{{ ticket.bus }}</a>
                  </h3>
                </div>
                <div class="product-price">
                  <ins>{{ ticket.price }}</ins>
                </div>
                <div class="product-rating"></div>
              </div>
            </div>
          </div>
          <!-- #shop end -->
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  props: ["ticket"],
};
</script>

<style scoped>
#text {
  text-align: left;
}
.product-price {
  margin: 0;
}
.container {
  margin: 0;
  padding: 0;
}
.product {
  padding: 0;
}
#product {
  padding: 2% 0 2% 2%;
}
.content-wrap {
  padding: 0;
}
</style>
