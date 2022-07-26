<script>
import Container from '@/components/layout/Container.vue';
export default {
    components: {
        Container
    },
    computed: {
        currentYear() {
           return new Date().getFullYear(); 
        }
    }
}
</script>

<template>
  <footer class="footer">
    <Container>
        <div class="socials">
            <a class="facebook" href="https://www.facebook.com/burntcoilband" name="To facebook" target="_blank">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 18 18" class="icon">
                    <path fill-rule="evenodd" d="M9 0a9 9 0 110 18A9 9 0 019 0zm2.606 4H10.24c-1.575 0-2.17.77-2.215 2.076l-.002.166v1.034H7V9h1.023V14h2.046V9h1.365l.181-1.724H10.07l.003-.862c0-.417.036-.655.553-.687l.128-.003h.853V4z"></path>
                </svg>
            </a>
            <a class="instagram" href="https://instagram.com/burntcoilband" name="To instagram" target="_blank">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 18 18" class="icon">
                    <path fill-rule="evenodd" d="M9 0a9 9 0 110 18A9 9 0 019 0zm1.128 4l-2.406.002-.468.011-.487.024c-.44.033-.76.112-1.042.222a2.45 2.45 0 00-.886.577 2.452 2.452 0 00-.577.886c-.123.318-.208.682-.232 1.214l-.021.58-.006.354v2.227l.013.648.024.487c.034.442.113.76.222 1.043.128.329.3.608.577.886.278.278.557.45.886.577.318.124.681.208 1.214.232l.524.02c.09.003.186.005.3.006h2.44c.164-.001.292-.004.412-.008l.176-.006.442-.022c.441-.033.76-.112 1.042-.222a2.45 2.45 0 00.886-.577c.278-.278.449-.557.577-.886.123-.318.208-.682.232-1.214l.02-.525.008-.485-.002-2.261-.017-.647-.02-.378a3.497 3.497 0 00-.221-1.043 2.452 2.452 0 00-.577-.886 2.45 2.45 0 00-.886-.577c-.318-.123-.681-.208-1.213-.232l-.58-.022A26.496 26.496 0 0010.127 4zm.893.927c.487.022.752.104.928.172.233.091.4.2.575.375.15.15.251.293.334.478l.04.097c.063.161.136.397.165.811l.026.588.005.27.005 1.58-.012 1.296c-.004.137-.01.264-.017.426-.02.447-.09.707-.155.883l-.017.046c-.09.233-.2.4-.374.575a1.549 1.549 0 01-.575.374 2.623 2.623 0 01-.811.165l-.672.028-.466.006-2.136-.001-.468-.009c-.133-.004-.258-.01-.416-.017-.488-.022-.753-.104-.929-.172-.233-.09-.4-.2-.575-.374a1.55 1.55 0 01-.374-.575 2.625 2.625 0 01-.165-.812l-.028-.672-.007-.794.002-1.809.014-.6.012-.285c.022-.487.104-.752.172-.928.09-.234.2-.4.374-.575a1.55 1.55 0 01.575-.375c.162-.062.398-.136.811-.165l.349-.017.234-.008c.12-.004.25-.006.419-.008h2.197c.437.003.623.01.96.026zM9.01 6.438a2.57 2.57 0 100 5.14 2.57 2.57 0 000-5.14zm0 .902a1.668 1.668 0 110 3.337 1.668 1.668 0 010-3.337zm2.649-1.616a.595.595 0 100 1.19.595.595 0 000-1.19z"></path>
                </svg>
            </a>
            <a class="youtube" href="https://www.youtube.com/channel/UCXtvuKYSM4U4DdhX6loEz3A/videos" name="To youtube" target="_blank">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 18 18" class="icon">
                    <path fill-rule="evenodd" d="M9 0a9 9 0 110 18A9 9 0 019 0zm.296 5l-1.12.006-.586.01c-.42.01-.89.023-1.34.045l-.334.017-.416.028-.183.027a1.26 1.26 0 00-.817.468c-.24.273-.352.796-.39 1.023l-.017.11-.056.716-.013.239-.02.528L4 8.455v1.09l.011.485c.014.366.037.696.055.923l.027.313.017.113c.04.23.15.749.39 1.02.375.46.875.424 1.093.495l.31.021c.178.01.39.02.617.027l1.416.04L9.12 13l.853-.009c.578-.009 1.327-.027 2.006-.064l.52-.033.184-.028a1.26 1.26 0 00.817-.468c.216-.245.328-.693.376-.946l.03-.186.056-.716c.015-.244.029-.53.035-.826l.003-.3v-.969l-.012-.485a21.84 21.84 0 00-.038-.705l-.044-.53-.01-.067c-.03-.196-.139-.775-.396-1.067a1.243 1.243 0 00-.717-.448l-.086-.017-.197-.03-.453-.03a61.382 61.382 0 00-2.751-.075zm-1.66 2l3.637 2-3.637 2V7z"></path>
                </svg>
            </a>
        </div>
        <p>© Burnt Coil {{ this.currentYear }}. All rights reserved.</p>
        <p class="credit">Website Built by <a href="https://www.meganfilo.dev" target="_blank">LoFi Web Designs</a></p>
    </Container>
  </footer>
</template>

<style lang="scss" scoped>
.footer {
    background: black;
    color: $color-text-50;
    font-size: $text-body-3;
    padding: $spacing-32 0;
    text-align: center;

    a { 
        color: $color-text-50;

        &:hover {
            text-decoration: underline;
        }
    }

    .credit {
        font-size: 12px
    }
}

.socials {
    display: flex;
    justify-content: center;
    margin-bottom: $spacing-16;

    a {
        display: block;
        max-width: 40px;
        width: 100%;

        &:not(:first-of-type) {
            margin-left: $spacing-16;
        }
    }

    .youtube {
        fill: #ff0000;
    }

    .facebook {
        fill: #3b5998;
    }

    .instagram {
        fill: #c13584;
    }
}
</style>