<template>
  <div id="collection-page-container">
    <v-col>
      <h3>Todas as coleções</h3>
    </v-col>

    <v-row>
      <v-col>
        <div class="slide-container">
          <span v-for="(collection, index) in allCollection" :key="index">
            <span class="slide-items">
              <img :src="require(`../assets/images/${collection.image}.jpg`)" />
              <span class="info-items">
                <p>{{ collection.name }}</p>
              </span>
            </span>
          </span>
        </div>
      </v-col>
    </v-row>
    <VerticalBar />
  </div>
</template>

<script>
import VerticalBar from "./verticalBar.vue";
export default {
  name: "AllCollectionSection",

  components: {
    VerticalBar,
  },

  data: () => ({
    allCollection: [
      { name: "Elia Nórdica", image: "Nordic Minimalist" },
      { name: "Solar Art", image: "stamped-ceramic-vases-c" },
      { name: "Fanny Verão", image: "ceremic-decor" },
    ],
  }),
};
</script>

<style scoped>
.slide-container {
  display: flex;
  flex-grow: 1;
  overflow: scroll;
  width: 100vw;
  padding: 0 15px;
  height: 35vh;
  justify-self: center;
}

.slide-items {
  margin: 10px;
  height: 30vh;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  width: 180px;
  cursor: pointer;
}

img {
  width: 100%;
  height: 25vh;
}

.info-items {
  display: flex;
  justify-content: space-between;
}

@media screen and (min-width: 815px) {
  .slide-container {
    overflow: hidden;
  }

  .slide-items {
    width: 200px;
  }

  .slide-container {
    justify-content: center;
  }

  img {
    width: 100%;
    height: 25vh;
  }
}
</style>
