<template>
  <div id="container">
    <HomeSection />
    <AboutSection />
    <CollectionSection />
    <MonthStorySection />
    <AllCollectionSection />
  </div>
</template>

<script>
import HomeSection from "./components/homeSection.vue";
import AboutSection from "./components/aboutSection.vue";
import CollectionSection from "./components/collectionSection.vue";
import MonthStorySection from "./components/StorySection.vue";
import AllCollectionSection from "./components/allCollectionSection.vue";

export default {
  name: "App",

  components: {
    HomeSection,
    AboutSection,
    CollectionSection,
    MonthStorySection,
    AllCollectionSection,
  },

  data: () => ({
    //
  }),
};
</script>
<style>
body {
  font-family: "Rubik", sans-serif;
  font-weight: 300;
}

h1 {
  font-weight: 400;
}

h2 {
  font-weight: 500;
}

h3 {
  font-weight: 600;
}
#container {
  overflow: hidden;
}
</style>
