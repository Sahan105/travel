<template>
  <div>
    <Navbar />
    <BlogSlider />
    <AllBlogs />
    <Footer />
  </div>
</template>

<script>
import Navbar from "../components/Navbar";
import BlogSlider from "../components/BlogSlider";
import AllBlogs from "../components/AllBlogs";
import Footer from "../components/Footer";
export default {
  components: {
    Navbar,
    AllBlogs,
    BlogSlider,
    Footer,
  },
};
</script>

<style></style>
