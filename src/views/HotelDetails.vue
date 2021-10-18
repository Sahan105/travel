<template>
    <Navbar />
    <p>{{ id }}</p>
    <div v-for="hotel in hotels" :key="hotel.id">
      <div v-if="this.id == hotel.id">
        <div
          class="entry clearfix"
          id="events"
        >
          <div id="main-title">
            <div class="entry-title">
              <h2>{{ hotel.name }}</h2>
            </div>
            <div class="entry-meta clearfix">
              <i class="icon-calendar3"></i> {{ hotel.date }}
            </div>
          </div>

          <div class="image" id="imgD">
            <div>
              <a href="#"><img :src="event.img1" alt="Blog Single" /></a>
            </div>
            <div id="details">
              {{ hotel.details }}
            </div>
          </div>
          <div class="entry-content notopmargin">
            <div class="clear"></div>
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
    <Footer />
</template>

<script>
import { mapState } from "vuex";
import Navbar from "../components/Navbar.vue";
import Footer from "../components/Footer.vue";
export default {
  props: ["id"],
  computed: {
    ...mapState("productbox", ["events"]),
  },
  components: {
    Navbar,
    Footer,
  },
};
</script>

<style scoped>
#events {
  display: flex;
  padding-left: -60%;
}
.image {
  widows: 50px;
}
#visit {
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
#related-details {
  padding: 0%;
}
#upcoming-event {
  padding: 0 5%;
}
#upcoming-event #h3 {
  padding: 2% 0;
  font-size: 3.5rem;
}
#imgD {
  margin-left: -35%;
}
#imgD img {
  margin-top: 2%;
  width: 560px;
  height: 400px;
}
#main-title {
  padding: 1% 14%;
  text-align: left;
}
</style>
