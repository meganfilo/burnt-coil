<script>
import { init } from 'aos';

import Container from '@/components/layout/Container.vue';

export default {
    components: {
        Container,
    },
    async asyncData({ $content }) {
        const doc = await $content('shows').fetch();
        return { doc };
    },
      head() {
    return {
      title: 'Shows | Burnt Coil',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Burnt Coil Upcoming Shows'
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
    <section class="shows">
        <Container>
            <h1>{{ doc.heading }}</h1>
            <div class="show-grid">
                <div class="show" v-for="show in doc.shows" :key="show.name">
                    <h3><strong>{{ show.date}} - {{show.time}}</strong></h3>
                    <p>{{ show.name }}</p>
                    <p>{{ show.location }}</p>
                    <a v-if="show.link_url" :href="show.link_url" target="_blank">Buy Tickets</a>
                </div>
            </div>
        </Container>
    </section>
</template>

<styles lang="scss" scoped>
.shows {
    background: black;
    color: $color-text-50;
    min-height: 100vh;

    h1 {
        font-size: $text-heading-1;
        font-weight: $font-weight-bold;
        color: $color-text-50;
        line-height: $line-height-heading-1;
    }

    .show-grid {
        width: 100%;
        text-align: center;
    }

    .show {
        margin-bottom: $spacing-24;

        h3, p, a {
            font-size: $text-body-3;
        }

        a {
            margin: $spacing-16 auto;
            display: block;
            width: 200px;
            text-align: center;
            color: $color-text-50;
            padding: $spacing-16;
            border: 1px solid $color-text-50;
        }

        @media (min-width: $breakpoint-lg) {
            display: flex;
            justify-content: space-between;
            gap: $spacing-24;
            align-items: center;

            a {
                margin: 0;
                flex: 0 1 15%;
            }
        }
    }
}
</styles>