<template>
  <div>
    <Navbar />
    <Hotel />
    <Footer />
  </div>
</template>

<script>
import Navbar from "../components/Navbar";
import Hotel from "../components/AllHotels";
import Footer from "../components/Footer";
export default {
  components: {
    Navbar,
    Hotel,
    Footer,
  },
};
</script>

<style></style>
