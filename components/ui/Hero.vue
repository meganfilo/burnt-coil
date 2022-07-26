<template>
  <section class="hero">
    <Container data-aos="fade-down" data-aos-duration="800">
        <img src="/images/logos/logo_large.webp" alt="Burnt Coil logo">
    </Container>
  </section>
</template>

<script>
import Container from '@/components/layout/Container.vue';
export default {
components: {
    Container
}
}
</script>

<style lang="scss" scoped>
.hero {
    background: $color-surface-black;
    color: $color-text-50;
    padding: $spacing-48 0;
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;

    @media (max-width: $breakpoint-md) {
        height: 40vh;
    }

    img {
        width: 100%;
    }
}
</style>