<script>
import Navigation from '~/components/navigation/Navigation';
import Footer from '@/components/navigation/Footer.vue';
export default {
    name: 'default',
    components: {
        Navigation,
        Footer
    }
}
</script>

<template>
  <div>
    <Navigation />
    <Nuxt role="main" />
    <Footer />
  </div>
</template>

<style>

   
</style>