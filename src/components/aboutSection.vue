<template>
  <div id="about-page-container">
    <v-col>
      <p class="about-text">
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae mollitia
        totam asperiores ratione ipsa, voluptates labore qui consequatur magnam
        ducimus!
      </p>
    </v-col>
    <VerticalBar class="divider" />
  </div>
</template>

<script>
import VerticalBar from "./verticalBar.vue";
export default {
  name: "AboutSection",

  components: {
    VerticalBar,
  },

  data: () => ({}),
};
</script>

<style scoped>
#about-page-container {
  padding: 70px 0;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.about-text {
  text-align: center;
  font-size: 18px;
  padding: 0 15px;
}
.divider {
  width: 60%;
}

@media screen and (min-width: 768px) {
  .about-text {
    text-align: center;
    padding: 0 30vw;
  }
  .divider {
    width: 60%;
  }
}
</style>
