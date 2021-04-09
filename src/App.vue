<template>
  <div id="app">
    <div class="section">
      <div class="container">
        <Navbar />
      </div>
    </div>
    <div class="columns">
      <Box />
    </div>
    <section class="main-content columns is-fullheight">
      <NavLateral />
      <section class="container">
        <div class="container">
          <div class="columns">
            <div class="column">
              <div class="notification fix-heigh">
                <!--Content-->
                <figure class="image center">
                  <img
                    src="./assets/fea-top-stats.svg"
                    style="max-width: 450px"
                  />
                </figure>
                <!--end-Content-->
              </div>
            </div>
            <div class="column">
              <div class="notification fix-heigh">
                <!--Content-->
                <figure class="image center">
                  <img src="./assets/statistic.jpg" style="max-width: 450px" />
                </figure>
                <!--end-Content-->
              </div>
            </div>
          </div>
        </div>
        <div class="columns">
          <div class="column">
            <div class="notification">
              <!--Content-->
              <div class="center">
                <BigCard />
              </div>
              <!--end-Content-->
            </div>
          </div>
        </div>
      </section>
    </section>
  </div>
</template>

<script>
import Navbar from "./components/Navbar";
import NavLateral from "./components/NavLateral";
import BigCard from "./views/BigCard";

export default {
  name: "App",
  components: {
    Navbar,
    NavLateral,
    BigCard,
  },
};
</script>

<style lang="sass">
@import "~bulma/bulma"

.center
  display: flex
  justify-content: center
  align-items: center
.fix-heigh
  height: 450px
</style>
