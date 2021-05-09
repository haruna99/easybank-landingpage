<template>
  <v-app>
    <v-main>
      <LandingPage />
    </v-main>
  </v-app>
</template>

<script>
import LandingPage from "./views/LandingPage";

export default {
  name: "App",

  components: {
    LandingPage,
  },

  data: () => ({
    //
  }),
};
</script>

<style lang="scss">
@import "@/assets/css/_media.scss";

  #app {
  font-family: Public Sans;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

  .header-text {
    color: hsl(233, 26%, 24%);
    font-weight: 400;
  }

  .main-text {
    color: hsl(233, 8%, 62%);
    font-size: 1.2rem;
  }

  *{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }

  html {
    font-size: 62.5%;
  }

  body {
    overflow-x: hidden;
  }
</style>
