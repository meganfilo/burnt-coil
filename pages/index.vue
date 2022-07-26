<script>
import Vue from 'vue';
import { init } from 'aos';
import Container from '@/components/layout/Container.vue';
import Hero from '@/components/ui/Hero.vue';
export default Vue.extend({
  name: 'IndexPage',
  components: {
    Hero,
    Container
  },
  head() {
    return {
      title: 'Burnt Coil',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Burnt Coil is a Neo-Soul/R&B band out of Milwaukee, WI. This nine-piece band brings a brass-heavy wall of sound backed by a tight and funky rhythm section.'
        }
      ]
    }
  },
  beforeMount() {
    init({
      once: true,
    });
  },
})
</script>

<template>
<div>
  <Hero />
  <section class="body">
    <Container>
      <h1>We are Burnt Coil.</h1>
      <p>
          Burnt Coil is a nine-piece Neo-Soul/R&B band based out of Milwaukee, WI comprised of members of various ages and music backgrounds.
      </p>
      <p>
          Playing around Southeastern Wisconsin, Burnt Coil brings a brass-heavy wall of sound backed by a tight and funky rhythm section. Despite their large size, the band is known for their ability to ditch the stage and bring the party into the crowd.
      </p>
    </Container>
  </section>
</div>
</template>

<style lang="scss" scoped>
.body {
  background: $secondary;
  color: $color-text-50;
  padding: $spacing-48 0;
  font-size: $text-body-1;

  @media (max-width: $breakpoint-md) {
    min-height: 60vh;
  }

  p {
    display: block;
    font-size: $text-body-1;
  }

  h1 {
    font-size: $text-heading-1;
    line-height: $line-height-heading-1;
    font-weight: $font-weight-bold;
  }
}
</style>
