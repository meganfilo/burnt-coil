<script>
import Close from './Close.vue';
import Hamburger from './Hamburger.vue';

export default {
  components: {
    Close,
    Hamburger,
  },
  data() {
    return {
      openMenu: false,
    };
  },
  computed: {
    containerStyle() {
      return this.openMenu
        ? 'position: absolute; transform: translateX(0);'
        : 'position: fixed; transform: translateX(100%);';
    },
  },
  methods: {
    toggleMobileNav() {
      this.openMenu = !this.openMenu;
    },
  },
};
</script>

<template>
  <div>
    <nav class="mobile-navigation">
      <div class="logo">
        <img src="/images/logos/logo.webp" alt="" aria-hidden="true" />
      </div>
      <button class="menu-toggle" @click="toggleMobileNav">
        <Hamburger v-if="!openMenu" />
        <Close v-else />
      </button>
    </nav>
    <div :style="containerStyle" class="menu">
    <ul class="links">
        <li><NuxtLink @click="toggleMobileNav" class="link" to="/">Home</NuxtLink></li>
        <li><NuxtLink @click="toggleMobileNav" class="link" to="/about">About</NuxtLink></li>
        <li><NuxtLink @click="toggleMobileNav" class="link" to="/shows">Shows</NuxtLink></li>
        <li><NuxtLink @click="toggleMobileNav" class="link" to="/contact">Contact</NuxtLink></li>
      </ul> 
    </div>
  </div>
</template>

<style lang="scss" scoped>
.mobile-navigation {
  background: $color-surface-black;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: nowrap;
  height: 50px;
  padding: 0 $spacing-8;
}

.menu-toggle {
  border: none;
  cursor: pointer;
  background: transparent;
}

.menu {
  transition: 0.3s all ease;
  width: 100%;
  background: $color-surface-black;
  color: $color-text-50;
  top: 50px;
  height: 100%;
  right: 0;
  padding: $spacing-16 $spacing-32;
  z-index: 3;
}

.links {
  text-align: right;
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 100%;
  list-style-type: none;

  li {
    margin-bottom: $spacing-24;
    font-size: $text-heading-5;

        a {
        color: $color-text-50;
     }
  }
}

.logo {
  display: inline;
  position: relative;
  max-width: 50px;

  img {
    width: 100%;
  }
}
</style>
