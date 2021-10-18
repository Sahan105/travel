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
                  ><img style="width: 280px; height: 370px" :src="event.img1" alt="Checked Short Dress"
                /></a>
                <a href="#"
                  ><img style="width: 280px; height: 370px" :src="event.img2" alt="Checked Short Dress"
                /></a>
                <div class="product-overlay">
                  <a href="#" class="add-to-cart"
                    ><i class="icon-shopping-cart"></i
                    ><span>Book Event</span></a
                  >
                  <a
                    href="include/ajax/shop-item.html"
                    class="item-quick-view"
                    data-lightbox="ajax"
                    ><i class="icon-zoom-in2"></i
                    ><span>View Event</span></a
                  >
                </div>
              </div>
              <div class="pt-3" id="text">
                <div class="product-title">
                  <h3>
                    <a href="#">{{ event.name }}</a>
                  </h3>
                </div>
                <div class="product-price">
                  <ins>{{ event.price }}</ins>
                </div>
                <div class="product-rating">
                
                </div>
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
  props: ["event"],
};
</script>

<style scoped>
  #text {
    text-align: left;
  }
  .product-price{
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
