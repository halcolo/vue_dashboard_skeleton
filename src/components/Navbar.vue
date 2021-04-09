<template>
  <div class="columns">
    <header class="navbar is-dark is-fixed-top is-transparent is-spaced">
      <div class="container">
        <div class="navbar-brand is-family-secondary">
          <a href="/" class="navbar-item">
            <span class="icon">
              <i class="fas fa-lg fa-home"></i>
            </span>
          </a>
          <a
            :aria-expanded="isActive"
            :class="{ 'is-active': isActive }"
            role="button"
            class="navbar-burger"
            aria-label="menu"
            data-target="collapse"
            @click="isActive = !isActive"
          >
            <span aria-hidden="true" />
            <span aria-hidden="true" />
            <span aria-hidden="true" />
          </a>
        </div>
        <div
          id="collapse"
          :class="{ 'is-active': isActive }"
          class="navbar-menu is-paddingless"
        >
          <nav class="navbar-end">
            <router-link class="navbar-item" to="/box">Home</router-link>
            <router-link class="navbar-item" to="/box">Box</router-link>
            <router-link class="navbar-item" to="/box">Others</router-link>
          </nav>
        </div>
      </div>
    </header>
  </div>
</template>

<script>
import throttle from "lodash/throttle";

export default {
  data() {
    return {
      isActive: false,
      showNavbar: true,
    };
  },
};
</script>

<style lang="sass" scoped>
.navbar
  height: 4rem

  .navbar-brand
    .navbar-burger
      height: 4.25rem

      span
        border-radius: 6px

  .navbar-item
    padding-top: 1rem
    padding-bottom: 1rem
</style>

