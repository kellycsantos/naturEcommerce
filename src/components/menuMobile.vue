<template>
  <div id="menu-mobile">
    <v-col cols="4">
      <v-menu offset-y>
        <template v-slot:activator="{ on, attrs }">
          <v-icon v-on="on" v-bind="attrs">mdi-menu</v-icon>
        </template>
        <v-col>
          <ul class="menu-mobile-container" my="50px">
            <li><a href="#">Natur</a></li>
            <li><a href="#">Sobre</a></li>
            <li><a href="#">Dashboard</a></li>
            <li><a href="#">Fale conosco</a></li>
          </ul>
        </v-col>
      </v-menu>
    </v-col>

    <v-col cols="4"><h1 class="menu-title">Natur eCommerce</h1></v-col>
    <v-col cols="4">
      <a href="">
        <v-icon>mdi-email-outline</v-icon>
      </a>
    </v-col>
  </div>
</template>

<script>
export default {
  name: "MenuMobile",

  data: () => ({}),
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  list-style: none;
  outline: none;
  border: none;
  text-decoration: none;
  box-sizing: border-box;
}
#menu-mobile {
  display: flex;
  justify-content: space-between;
  align-items: center;
  text-align: center;
}
.v-menu__content {
  margin-top: 30px;
  width: 75vw;
  display: flex;
  flex-direction: column;
  justify-self: center;
  background: rgb(255, 255, 255);
}

.v-menu__content a {
  display: flex;
  border: 1px solid black;
  align-items: center;
  height: 50px;
  margin-bottom: 5px;
  color: black;
  padding: 2px;
}
.menu-title {
  font-size: 18px;
}

@media screen and (min-width: 768px) {
  #menu-mobile {
    display: none;
  }
}
</style>
