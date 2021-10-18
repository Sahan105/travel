<template>
  <div class="shopdetails">
    <section id="content">
      <div class="content-wrap">
        <div class="container clearfix">
          <div
            id="shop"
            class="shop grid-container clearfix"
            data-layout="fitRows"
          >
            <div
              class="product clearfix"
              v-for="content in contents"
              :key="content"
            >
              <div class="product-image">
                <a href="#"
                  ><img :src="content.img1" alt="Checked Short Dress"
                /></a>
                <a href="#"
                  ><img :src="content.img2" alt="Checked Short Dress"
                /></a>
                <div class="product-overlay">
                  <a href="#" class="add-to-cart"
                    ><i class="icon-shopping-cart"></i
                    ><span>{{ content.cart }}</span></a
                  >
                  <a
                    href="include/ajax/shop-item.html"
                    class="item-quick-view"
                    data-lightbox="ajax"
                    ><i class="icon-zoom-in2"></i
                    ><span> {{ content.view }}</span></a
                  >
                </div>
              </div>
              <div class="product-desc">
                <div class="product-title">
                  <h3>
                    <a href="#">{{ content.h1 }}</a>
                  </h3>
                </div>
                <div class="product-price">
                  <del>$24.99</del> <ins>{{ content.prize }}</ins>
                </div>
                <div class="product-rating">
                  <i
                    v-for="i in parseInt(content.rating)"
                    :key="'f' + i"
                    class="icon-star3"
                  ></i>
                  <i
                    v-for="j in 5 - parseInt(content.rating)"
                    :key="'ff' + j"
                    class="icon-star-empty"
                  ></i>
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
import { mapState } from "vuex";
export default {
  computed: {
    ...mapState("shopdeatils", ["contents"]),
  },
};
</script>
