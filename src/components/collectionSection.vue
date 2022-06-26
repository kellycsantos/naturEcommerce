<template>
  <div id="collection-page-container">
    <v-col>
      <h3>Nova coleção</h3>
    </v-col>
    <v-row>
      <v-col>
        <div class="slide-container">
          <span v-for="(product, index) in newProducts" :key="index">
            <span class="slide-items">
              <img :src="require(`../assets/images/${product.image}.jpg`)" />
              <span class="info-items">
                <p>{{ product.name }}</p>
                <p>R$ {{ product.price }}</p>
              </span>
            </span>
          </span>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "CollectionSection",

  components: {},

  data: () => ({
    newProducts: [
      { name: "Asian Ceramic", image: "ceramic-asian-art", price: "152" },
      { name: "Vasos Ophelia", image: "ophelia-vases", price: "189" },
      { name: "Chápei", image: "ceramic-pieces-collection", price: "95" },
      { name: "Douja Ten", image: "ceramic-vase-modern", price: "127" },
      { name: "Fah C", image: "blomus-ceolo ceramic-vase", price: "219" },
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
