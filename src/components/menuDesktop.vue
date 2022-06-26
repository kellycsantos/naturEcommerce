<template>
  <div id="menu-desktop">
    <v-col>
      <ul class="menu-desktop-container">
        <li><a href="#">Natur</a></li>
        <li><a href="#">Sobre</a></li>
        <li><h1 class="menu-title">Natur eCommerce</h1></li>
        <li><a href="#">Dashboard</a></li>
        <li><a href="#">Fale conosco</a></li>
      </ul>
    </v-col>
  </div>
</template>

<script>
export default {
  name: "MenuDesktop",

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
.menu-desktop-container {
  display: none;
}

@media screen and (min-width: 768px) {
  .menu-desktop-container {
    width: 100vw;
    height: 70px;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
  }

  .menu-desktop-container a {
    display: flex;
    align-items: center;
    height: 20px;
    margin-bottom: 5px;
    color: black;
    padding: 5px;
  }

  .menu-desktop-container a:hover {
    color: rgb(107, 61, 5);
  }

  .menu-title {
    font-size: 22px;
    font-weight: 300;
  }
}
</style>
