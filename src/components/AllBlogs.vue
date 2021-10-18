<template>
  <div class="container clearfix">
    <div class="col_three_fifth bothsidebar nobottommargin">
      <div class="fancy-title title-border" id="title">
        <h3>Blogs</h3>
      </div>
      <div id="posts" class="events small-thumbs">
        <Blogcart />
      </div>
    </div>

    <div class="col_two_fifth nobottommargin col_last" id="gallery">
      <div class="fancy-title title-border">
        <h4>Search For Blogs</h4>
      </div>
      <div class="search">
        <form>
          <input type="text" placeholder="Search.." name="search" />
          <button id="myButton" type="submit"><i> Search</i></button>
        </form>
      </div>
      <div class="fancy-title title-border">
        <h4>Video</h4>
      </div>
      <div>
        <iframe
          width="560"
          height="315"
          src="https://www.youtube.com/embed/oXNVtSEhS-Q"
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
import Blogcart from "../components/AllBlogs";
export default {
  name: "productbox",
  computed: {},
  components: {
    Blogcart,
  },
};
</script>

<style scoped>
.img {
  height: 100px;
}
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
