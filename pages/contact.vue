<script>
import Container from '@/components/layout/Container.vue';

export default {
    components: {
        Container,
    },
      head() {
    return {
      title: 'Contact | Burnt Coil',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Get in touch with Burnt Coil'
        }
      ]
    }
  },
}
</script>

<template>
  <section class="contact">
    <Container>
        <h1>Keep in touch!</h1>
        <p>Follow us on our socials, fill out the form below, or reachout to us at burntcoilband@gmail.com.</p>
    
        <form name="contact" method="POST" data-netlify="true" data-netlify-recaptcha="true">
  <p>
    <label>Your Name: </label>
    <input type="text" name="name" />
  </p>
  <p>
    <label>Your Email:</label>
     <input type="email" name="email" />
  </p>
  <p>
    <label>Message: </label>
    <textarea name="message"></textarea>
  </p>
  <p>
    <button type="submit">Submit</button>
  </p>
</form>
    </Container>
  </section>
</template>

<style lang="scss" scoped>
.contact {
    background: black;
    min-height: 80vh;
    color: $color-text-50;

    h1 {
        font-size: $text-heading-1;
        font-weight: $font-weight-bold;
        color: $color-text-50;
        line-height: $line-height-heading-1;
    }

    p {
        font-size: $text-body-1;
        line-height: $line-height-body-1;
    }

    form {
        margin-top: $spacing-64;

        label {
            display: block;
            text-transform: uppercase;
            color: $color-text-100;
            font-size: 14px;
            line-height: 14px;
            margin-bottom: $spacing-8;
        }
        
        input, textarea {
            margin-bottom: $spacing-24;
            width: 100%;
            max-width: 500px;

            @media (max-width: $breakpoint-md) {
                height: 40px;
            }
        }

        button {
            cursor: pointer;
            background: transparent;
            display: block;
            width: 200px;
            text-align: center;
            color: $color-text-50;
            padding: $spacing-16;
            border: 1px solid $color-text-50;
            transition: all 0.3s ease;

            &:hover {
                border: 1px solid black;
                background: $color-surface-50;
                color: black;
            }
        }
    }
}
</style>