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
            <div class="product clearfix">
              <div class="product-image">
                <a href="#"
                  ><img
                    style="width: 280px; height: 370px"
                    :src="hotel.img1"
                    alt="Checked Short Dress"
                /></a>
                <a href="#"
                  ><img
                    style="width: 280px; height: 370px"
                    :src="hotel.img2"
                    alt="Checked Short Dress"
                /></a>
                <div class="product-overlay">
                  <a href="#" class="add-to-cart"
                    ><i class="icon-shopping-cart"></i><span></span
                  ></a>
                  <a
                    href="include/ajax/shop-item.html"
                    class="item-quick-view"
                    data-lightbox="ajax"
                    ><i class="icon-zoom-in"></i><span></span
                  ></a>
                </div>
              </div>
              <div id="text">
                <div class="product-title">
                  <h3>
                    <a href="#">{{ hotel.name }}</a>
                  </h3>
                </div>
                <div class="product-price">
                  <ins>{{ hotel.price }}</ins>
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
  props: ["hotel"],
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
.content-wrap {
  padding: 0;
}
</style>
