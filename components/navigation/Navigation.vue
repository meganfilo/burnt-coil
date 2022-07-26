      <template>
        <header class="header">
          <div class="desktop-nav-wrapper">
            <DesktopNav />
          </div>
          <div class="mobile-nav-wrapper">
            <MobileNav />
          </div>
        </header>
      </template>
      
      <script>
      import MobileNav from './MobileNav.vue'
      import DesktopNav from './DesktopNav.vue';
      export default {
        components: {
          MobileNav,
          DesktopNav,
        }
      }
      </script>
      
      <style lang="scss" scoped>
        .desktop-nav-wrapper {
          display: block;
        }

        .mobile-nav-wrapper {
          display: none;
        }

        @media (max-width: $breakpoint-md) {
          .desktop-nav-wrapper {
            display: none;
          }
          .mobile-nav-wrapper {
            display: block;
          }
        }
      </style>