<template>
  <div class="container">
    <header class="header">
      <div class="header__cover">
        <h1 class="header__name">Solutions for people <br />like you</h1>
      </div>
    </header>
    <main class="main">
      <div class="wrapper">
        <XCard category="| marketing">
          <div style="background-color: #d3d8e4; height: 100%"></div>
        </XCard>
        <XCard>
          <img src="./assets/img2.jpg" alt="" />
        </XCard>
        <XCard category="| marketing" color="dark">
          <div style="background-color: #ff779a; height: 100%"></div>
        </XCard>
        <XCard category="| marketing" color="dark">
          <div style="background-color: #00b6dd; height: 100%"></div>
        </XCard>
        <XCard category="| marketing">
          <img src="./assets/img1.jpg" alt="" />
        </XCard>
        <XCard color="dark">
          <div style="background-color: #d3d8e4; height: 100%"></div>
        </XCard>
      </div>
    </main>
    <footer></footer>
  </div>
</template>

<script>
import XCard from "./components/XCard.vue";

export default {
  name: "App",
  components: {
    XCard,
  },
};
</script>

<style lang="scss">
@import "./style/style.scss";
</style>
