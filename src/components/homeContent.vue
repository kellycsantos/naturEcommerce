<template>
  <div id="content-container">
    <v-row>
      <v-col>
        <h2>nova<br />coleção</h2>
      </v-col>
    </v-row>

    <v-row>
      <v-col>
        <h3>Adquira</h3>
        <v-col>
          <vertical-bar class="divider"></vertical-bar>
        </v-col>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import verticalBar from "./verticalBar.vue";
import VerticalBar from "./verticalBar.vue";
export default {
  components: { verticalBar },
  name: "HomeContent",
  componets: {
    VerticalBar,
  },
  data: () => ({}),
};
</script>

<style scoped>
#content-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  height: 40vh;
  margin-top: 100px;
}

h3 {
  cursor: pointer;
}
.divider {
  margin-top: -25px;
  width: 110px;
}
</style>
