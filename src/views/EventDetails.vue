<template>
  <div>
    <Navbar />
    <p>{{ id }}</p>
    <div v-for="event in events" :key="event.id">
      <div v-if="this.id == event.id">
        <div
          class="entry clearfix"
          id="events
    "
        >
          <div id="main-title">
            <div class="entry-title">
              <h2>{{ event.h1 }}</h2>
            </div>
            <div class="entry-meta clearfix">
              <i class="icon-calendar3"></i> {{ event.date }}
            </div>
          </div>

          <div class="image" id="imgD">
            <div>
              <a href="#"><img :src="event.img1" alt="Blog Single" /></a>
            </div>
            <div id="details">
              {{ event.details }}
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
    <div id="upcoming-event">
      <h3 id="h3">Upcoming Events</h3>
      <div class="related-posts clearfix">
        <div class="shop grid-container clearfix" data-layout="fitRows">
          <div class="product clearfix" v-for="event in events" :key="event">
            <div class="product-image">
              <router-link
                :to="{ name: 'EventDetails', params: { id: event.id } }"
              >
                <img :src="event.img1" alt="Checked Short Dress" />
              </router-link>
              <router-link
                :to="{ name: 'EventDetails', params: { id: event.id } }"
              >
                <img :src="event.img2" alt="Checked Short Dress" />
              </router-link>
              <div class="product-overlay">
                <a href="#" class="add-to-cart"
                  ><i class="icon-shopping-cart"></i
                  ><span>{{ event.cart }}</span></a
                >
                <router-link
                  :to="{ name: 'EventDetails', params: { id: event.id } }"
                  class="item-quick-view"
                  data-lightbox="ajax"
                  ><i class="icon-zoom-in2"></i><span> {{ event.view }}</span>
                </router-link>
              </div>
            </div>
            <div class="product-desc">
              <div class="product-title">
                <h3>
                  <router-link
                    :to="{ name: 'EventDetails', params: { id: event.id } }"
                  >
                    {{ event.h1 }}
                  </router-link>
                </h3>
              </div>
              <div class="product-price">
                <h3>
                  <a href="">{{ event.prize1 }}</a>
                </h3>
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
