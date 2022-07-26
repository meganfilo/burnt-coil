<template>
  <div class="container">
    <slot></slot>
  </div>
</template>

<script lang="ts">
export default {
  name: "Container",
};
</script>

<style lang="scss" scoped>
@import '~/styles/variables.scss';
.container {
  width: 100%;
  margin-left: auto;
  margin-right: auto;
  padding-left: $spacing-16;
  padding-right: $spacing-16;
  border: 1px solid transparent;
}

@media (min-width: 640px) {
  .container {
    max-width: 95%;
  }
}

@media (min-width: 1024px) {
  .container {
    max-width: 1024px;
    padding: 0px;
  }
}

@media (min-width: 1170px) {
  .container {
    max-width: 1170px;
    padding: 0px;
  }
}
</style>
