<template>
  <div>
    <Navbar />
    <AboutDetails />
    <Team />
    <Footer />
  </div>
</template>
<script>
import Navbar from "../components/Navbar";
import AboutDetails from "../components/About-Details";
import Team from "../components/Team";
import Footer from "../components/Footer";

export default {
  components: {
    Navbar,
    AboutDetails,
    Team,
    Footer,
  },
};
</script>
<style></style>
