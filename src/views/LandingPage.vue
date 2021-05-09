<template>
    <div id="landingpage">
      <Navbar />
      <div class="main-content">
          <!-- <div class="intro-images"> -->
              <!-- <img src="../assets/img/bg-intro-desktop.svg" alt="" class="image-1">
              <img src="../assets/img/image-mockups.png" alt="" class="image-2"> -->
          <!-- </div> -->
          <div class="main-body">
              <Introduction />
              <WhyEasy />
              <LatestArticles />
          </div>
      </div>
      <Footer />
    </div>
</template>

<script>
import WhyEasy from "../layout/WhyEasy";
import Introduction from "../layout/Introduction";
import LatestArticles from "../layout/LatestArticles";
import Navbar from "../layout/Navbar";
import Footer from "../layout/Footer";

export default {
    components: {
        Navbar,
        Introduction,
        WhyEasy,
        LatestArticles,
        Footer,
    }
}
</script>

<style lang="scss">
    #landingpage {

        .main-content {
            position: relative;
        }
    }
</style>