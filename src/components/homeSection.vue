<template>
  <div id="home-page-container">
    <MenuMobile data-app />
    <MenuDesktop />
    <HomeContent />
  </div>
</template>

<script>
import MenuMobile from "./menuMobile.vue";
import MenuDesktop from "./menuDesktop.vue";
import HomeContent from "./homeContent.vue";

export default {
  name: "HomeSection",

  components: {
    MenuMobile,
    MenuDesktop,
    HomeContent,
  },

  data: () => ({}),
};
</script>

<style scoped>
#home-page-container {
  background: #dfdedc url("../assets/images/ceramic-pieces-collection.jpg")
    no-repeat bottom;
  background-size: cover;
  height: 100vh;
  padding-top: 30px;
}

@media screen and (min-width: 768px) {
  #home-page-container {
    background-size: cover;
  }
}
@media screen and (min-width: 1264px) {
  #home-page-container {
    background-position: center;
  }
}
</style>
