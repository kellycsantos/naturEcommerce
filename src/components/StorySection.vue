<template>
  <div id="collection-page-container">
    <v-row>
      <v-col>
        <div id="story-container">
          <div class="story-content">
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Harum
              beatae eum quidem.
            </p>
            <h3>conto do mês</h3>
            <vertical-bar class="divider"></vertical-bar>
          </div>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import VerticalBar from "./verticalBar.vue";
export default {
  name: "MonthStorySection",

  components: {
    VerticalBar,
  },

  data: () => ({}),
};
</script>

<style scoped>
#story-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background: url("../assets/images/bowl-trace.jpg") center;
  background-size: 100%;
  height: 30vh;
  width: 80vw;
  margin: 5px 10vw;
  border-radius: 5px;
}

#story-container p {
  display: none;
}
.story-content {
  display: flex;
  flex-direction: column;
  align-items: center;
}

h3 {
  cursor: pointer;
}

.divider {
  width: 120px;
  margin-top: -20px;
}

@media screen and (min-width: 768px) {
  #story-container {
    display: flex;
    flex-direction: column;
    align-items: end;
    justify-content: center;
    background: url("../assets/images/bowl-trace.jpg") left center no-repeat;
    background-size: clamp(200px, 50%, 600px);
    height: 50vh;
    width: 80vw;
    margin: 5px 10vw;
    border-radius: 5px;
  }

  .story-content {
    display: block;
  }

  #story-container p {
    display: block;
    width: 30vw;
    margin-bottom: 30px;
  }

  .divider {
    width: 155px;
    margin: -20px 0 0 -13px;
  }
}
</style>
