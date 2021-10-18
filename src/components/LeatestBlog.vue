<template>
  <div class="blog">
    <div class="section notopmargin notopborder" id="section">
    <div class="container clearfix">
      <div class="heading-block center nomargin">
        <h3>Latest from the Blog</h3>
      </div>
    </div>
    </div>

    <div id="shop" class="grid-container clearfix">
      <div class="product clearfix">
        <BlogCart />
      </div>
    </div>
  </div>
</template>
<script>
import BlogCart from "../components/carts/BlogCart";
export default {
  computed: {},
  components: {
    BlogCart,
  },
};
</script>
<style scoped>
.blog {
  text-align: center;
}
#section {
  margin: 0;
}

</style>
