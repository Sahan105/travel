<template>
  <div>
    <Navbar />
    <p>{{ id }}</p>
    <div v-for="blog in blogs" :key="blog.id">
      <div v-if="this.id == blog.id">
        <div class="entry clearfix" id="image-details">
          <div id="main-title">
            <div class="entry-title">
              <h2>{{ blog.title }}</h2>
            </div>
            <div class="entry-meta clearfix">
              <i class="icon-calendar3"></i> {{ blog.date }}
            </div>
          </div>

          <div class="image" id="imgD">
            <div>
              <a href="#"><img :src="blog.src" alt="Blog Single" /></a>
            </div>
            <div id="details">
              {{ blog.details }}
            </div>
          </div>
          <div class="entry-content notopmargin">
            <div class="si-share noborder clearfix" id="visit">
              <div id="h1">
                <span>Visit Us On</span>
              </div>
              <div id="icon">
                <a href="#" class="social-icon si-borderless si-facebook">
                  <i class="icon-facebook"></i>
                  <i class="icon-facebook"></i>
                </a>
                <a href="#" class="social-icon si-borderless si-pinterest">
                  <i class="icon-instagram"></i>
                  <i class="icon-instagram"></i>
                </a>
                <a href="#" class="social-icon si-borderless si-gplus">
                  <i class="icon-youtube"></i>
                  <i class="icon-youtube"></i>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div id="upcoming-event">
      <h3 id="h3">Related Blogs</h3>
      <div class="related-posts clearfix">
        <div class="shop grid-container clearfix">
          <div
            id="blog-details"
            v-for="(blog, index) in blogs"
            :key="index"
            class="product clearfix"
          >
            <div class="entry clearfix" id="infrom-details">
              <div class="entry-title" id="b-title">
                <h3>{{ blog.title }}</h3>
              </div>
              <div class="entry-meta clearfix" id="b-date">
                <i class="icon-calendar3"></i> {{ blog.date }}
              </div>
              <div class="related-image">
                <a href="#"><img :src="blog.src" alt="Blog Single" /></a>
              </div>
              <div id="b-details">
                {{ blog.details }}
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import { mapState } from "vuex";
import Navbar from "../components/Navbar.vue";
import Footer from "../components/Footer.vue";
export default {
  props: ["id"],
  computed: {
    ...mapState("productbox", ["blogs"]),
  },
  components: {
    Navbar,
    Footer,
  },
};
</script>

<style scoped>
.image {
  padding: 2%;
  height: 60px;
  widows: 50px;
}
#main-title {
  padding: 1% 14%;
  text-align: left;
}
#visit {
  margin-top: 35%;
  margin-left: 13%;
  display: flex;
  justify-content: flex-start;
}
#visit span {
  font-size: 2rem;
}
#visit i {
  font-size: 1.8rem;
}
#details {
  padding: 1% 30%;
  text-align: left;
  margin-left: 6%;
}
.related-image {
  height: 300px;
  width: 300px;
}
#upcoming-event {
  margin-top: -3%;
  padding: 0 3%;
}
#blog-details {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
}
#infrom-details {
  display: grid;
  height: 560px;
  grid-template-rows: repeat(4, 1fr);
}
#upcoming-event #h3 {
  padding-top: 2%;
  font-size: 3rem;
}
#related-details {
  padding: 0%;
}
#b-date {
  margin-top: -5%;
}
#imgD {
  margin-left: -35%;
}
#imgD img {
  margin-top: 2%;
  width: 560px;
  height: 400px;
}
#b-details {
  margin-top: -25%;
}
</style>
