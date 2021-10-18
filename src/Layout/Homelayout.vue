<template>
  <div>
    <Navbar />
    <Slider />
    <Events />
    <Hotels />
    <LatestBlog />
    <Footer />
  </div>
</template>
<script>
import Events from "../components/Featured-Events";
import Navbar from "../components/Navbar";
import Slider from "../components/Slider";
import Hotels from "../components/Featured-Hotels";
import Footer from "../components/Footer1";
import LatestBlog from "../components/LeatestBlog";
import SliderTwo from "../components/SliderTwo";

export default {
  components: {
    Navbar,
    Slider,
    Hotels,
    Footer,
    LatestBlog,
    Events,
    SliderTwo,
  },
};
</script>
<style scoped></style>
