<template>
  <div class="container clearfix">
    <div class="col_three_fifth bothsidebar nobottommargin">
      <div class="fancy-title title-border" id="title">
        <h3>Upcoming Events</h3>
      </div>
      <div id="posts" class="events small-thumbs">
        <div v-for="event in events" :key="event">
          <div class="entry clearfix">
            <div class="entry-image hidden-sm">
              <router-link
                :to="{ name: 'EventDetails', params: { id: event.id } }"
              >
                <img
                  :src="event.img"
                  alt="Inventore voluptates velit totam ipsa tenetur"
                />
              </router-link>
            </div>
            <div class="entry-c">
              <div class="entry-title">
                <h2>
                  <router-link
                    :to="{ name: 'EventDetails', params: { id: event.id } }"
                  >
                    {{ event.title }}
                  </router-link>
                </h2>
              </div>
              <ul class="entry-meta clearfix">
                <li><i class="icon-time"></i> {{ event.date }}</li>
                <li><i class="icon-map-marker2"></i> {{ event.location }}</li>
              </ul>
              <div class="entry-content">
                <a href="#" class="btn btn-default" disabled="disabled"
                  >Buy Tickets</a
                >
                <router-link
                  :to="{ name: 'EventDetails', params: { id: event.id } }"
                  class="btn btn-danger"
                  >Read More</router-link
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="col_two_fifth nobottommargin col_last" id="gallery">
      <div class="fancy-title title-border">
        <h4>Search For Events</h4>
      </div>
      <div class="search">
        <form>
          <input type="text" placeholder="Search.." name="search" />
          <button id="myButton" type="submit"><i> Search</i></button>
        </form>
      </div>
      <div class="fancy-title title-border">
        <h4>Gallery</h4>
      </div>
      <div
        class="col_full masonry-thumbs col-4 clearfix"
        data-lightbox="gallery"
      >
        <a href="images/events/1.jpg" data-lightbox="gallery-item"
          ><img
            class="image_fade"
            src="images/events/thumbs/1.jpg"
            alt="Gallery Thumb 1"
        /></a>
        <a href="images/events/2.jpg" data-lightbox="gallery-item"
          ><img
            class="image_fade"
            src="images/events/thumbs/2.jpg"
            alt="Gallery Thumb 2"
        /></a>
        <a href="images/events/3.jpg" data-lightbox="gallery-item"
          ><img
            class="image_fade"
            src="images/events/thumbs/3.jpg"
            alt="Gallery Thumb 3"
        /></a>
        <a href="images/events/4.jpg" data-lightbox="gallery-item"
          ><img
            class="image_fade"
            src="images/events/thumbs/4.jpg"
            alt="Gallery Thumb 4"
        /></a>
        <a href="images/events/5.jpg" data-lightbox="gallery-item"
          ><img
            class="image_fade"
            src="images/events/thumbs/5.jpg"
            alt="Gallery Thumb 5"
        /></a>
        <a href="images/events/6.jpg" data-lightbox="gallery-item"
          ><img
            class="image_fade"
            src="images/events/thumbs/6.jpg"
            alt="Gallery Thumb 6"
        /></a>
        <a href="images/events/7.jpg" data-lightbox="gallery-item"
          ><img
            class="image_fade"
            src="images/events/thumbs/7.jpg"
            alt="Gallery Thumb 7"
        /></a>
        <a href="images/events/8.jpg" data-lightbox="gallery-item"
          ><img
            class="image_fade"
            src="images/events/thumbs/8.jpg"
            alt="Gallery Thumb 8"
        /></a>
      </div>
      <div class="fancy-title title-border">
        <h4>Video</h4>
      </div>
      <div>
        <iframe
          width="560"
          height="315"
          src="https://www.youtube.com/embed/58LJm8O6QhM"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </div>
    </div>
  </div>
</template>

<script>
import { mapState } from "vuex";
export default {
  name: "productbox",
  computed: {
    ...mapState("eventsdetails", ["events"]),
  },
};
</script>

<style scoped>
#title {
  padding-top: 10%;
}
#gallery {
  padding-top: 4%;
}
.search {
  margin-top: 8px;
  margin-right: 16px;
  font-size: 2rem;
  border: none;
  cursor: pointer;
  padding-bottom: 6px;
}
#myButton {
  display: inline-block;
  cursor: pointer;
  font-size: 1.6rem;
  padding: 6px 14px 4px 14px;
  background-color: #ce4c48;
  border-radius: 3px;
  color: #2c3e50;
  border: none;
  font: sans-serif;
}
#myButton:hover {
  background-color: #c9302c;
}
</style>
