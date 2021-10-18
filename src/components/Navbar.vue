<template>
  <div id="nav">
    <div class="brand">
      <router-link to="/">Canvas</router-link>
    </div>
    <div class="main-nav">
      <router-link v-for="item in list" :key="item" :to="item.to">{{
        item.title
      }}</router-link>
    </div>
  </div>
</template>

<script>
import { mapState } from "vuex";
export default {
  name: "navbar",
  computed: {
    ...mapState("navbar", ["list"]),
  },
};
</script>

<style scoped>
* {
  padding: 0;
  margin: 0;
  outline: 0;
}
#nav {
  padding: 2.5% 5%;
  display: flex;
  z-index: 10;
}
.main-nav {
  margin-left: 40%;
  font-size: 1.8rem;
}
.brand {
  font-size: 2.3rem;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
}
li {
  display: inline-block;
  margin: 0 10px;
}

.main-nav a {
  color: #42b983;
  padding: 2rem;
}
</style>
