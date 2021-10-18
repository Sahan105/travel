<template>
  <div class="eventlayout">
    <Navbar />
    <EventSlider />
    <Events />
    <Footer />
  </div>
</template>
<script>
import Navbar from "../components/Navbar";
import Footer from "../components/Footer";
import Events from "../components/UpcommingEvents";
import EventSlider from "../components/EventSlider"

export default {
  components: {
    Navbar,
    Footer,
    Events,
    EventSlider
  },
};
</script>
