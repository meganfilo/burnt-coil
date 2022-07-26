<script>
export default {

};
</script>

<template>
  <nav class="desktop-navigation">
    <div class="logo">
      <img src="/images/logos/logo.webp" alt="" aria-hidden="true" />
    </div>
    <ul class="links">
        <li><NuxtLink class="link" to="/">Home</NuxtLink></li>
        <li><NuxtLink class="link" to="/about">About</NuxtLink></li>
        <li><NuxtLink class="link" to="/shows">Shows</NuxtLink></li>
        <li><NuxtLink class="link" to="/contact">Contact</NuxtLink></li>
      </ul> 
  </nav>
</template>

<style lang="scss" scoped>
.desktop-navigation {
  background: $color-surface-black;
  padding: $spacing-16 $spacing-48;
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  justify-content: space-between;
  align-items: center;
  gap: $spacing-16;

  @media (max-width: 900px) {
    gap: $spacing-8;
  }
}

.links {
  display: flex;
  gap: $spacing-64;
  align-items: center;
  list-style-type: none;

  li {
    font-size: $text-heading-5;
     a {
color: $color-text-50;
font-weight: $font-weight-bold;
     }
  }
}
.logo {
  display: inline;
  position: relative;
  max-width: 100px;

  img {
    width: 100%;
  }
}
</style>
