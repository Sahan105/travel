<template>
  <section id="content">
    <div class="content-wrap">
      <div class="container clearfix">
        <div
          class="col_one_third nobottommargin col_last"
          v-for="blog in blogs"
          :key="blog"
        >
          <div class="feature-box media-box">
            <div class="fbox-media">
              <img :src="blog.img" alt="Why choose Us?" />
            </div>
            <div class="fbox-desc" id="fbox-desc">
              <h3>{{ blog.title }}</h3>
              <span class="date">{{ blog.date }}</span>
              <p class="pt-2">{{ blog.short_description }}... <a href="/blogs/:id">see more</a></p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { mapState } from "vuex";
export default {
  computed: {
    ...mapState("productbox", ["blogs"]),
  },
};
</script>
<style scoped>
#fbox-desc {
  color: #42424299;
  text-align: left;
}
#fbox-desc span {
  font-family: "Lato", sans-serif;
}
#fbox-desc h3 {
  font-size: 2rem;
  font-family: "Lato", sans-serif;
}
#fbox-desc p {
  font-size: 1.8rem;
  margin: 0;
}
#content #title {
  font-family: "Lato", sans-serif;
  font-size: 2.5rem;
}
.col_last {
  padding: 0 1%;
}
.container {
  padding: 0;
}
</style>

<style></style>
