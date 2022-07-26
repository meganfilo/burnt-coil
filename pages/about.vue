<script>
import { init } from 'aos';

import Container from '@/components/layout/Container.vue';
import BandCard from '@/components/ui/BandCard.vue';

export default {
    components: {
        Container,
        BandCard
    },
    async asyncData({ $content }) {
        const doc = await $content('bio').fetch();
        return { doc };
    },
      head() {
    return {
      title: 'About | Burnt Coil',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Meet the band members of Burnt Coil'
        }
      ]
    }
  },
    beforeMount() {
    init({
      once: true,
    });
  },
}
</script>

<template>
    <section class="about">
        <Container>
            <div data-aos="fade-left"
              data-aos-duration="1200">
                <h1>{{ doc.heading }}</h1>
                <div v-if="doc.body_text" class="subtitle" v-html="$md.render(doc.body_text)"></div>
            </div>

            <div class="member-grid">
                <BandCard v-for="(member, index) in doc.members" :key="member.name" :data="member" data-aos-duration="800" :data-aos="(index % 2 ) == 1 ? 'fade-right' : 'fade-left'" />
            </div>
        </Container>
    </section>
</template>

<style lang="scss" scoped>
.about {
    background: black;
    color: $color-text-50;

    h1 {
        font-size: $text-heading-1;
        font-weight: $font-weight-bold;
        color: $color-text-50;
        line-height: $line-height-heading-1;

    }

    .subtitle {
        font-size: $text-heading-4;
        line-height: $line-height-heading-4;
    }
}

.member-grid {
    margin-top: $spacing-64;
    margin-bottom: $spacing-64;
}
</style>