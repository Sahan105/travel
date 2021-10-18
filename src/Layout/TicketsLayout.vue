<template>
  <div>
    <Navbar />
    <Tickets />
    <Footer />
  </div>
</template>

<script>
import Navbar from "../components/Navbar";
import Tickets from "../components/AllTickets";
import Footer from "../components/Footer";
export default {
  components: {
    Navbar,
    Tickets,
    Footer,
  },
};
</script>

<style></style>
