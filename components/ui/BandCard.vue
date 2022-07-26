<script>
export default {
    props: {
        data: {
            type: Object,
            required: true,
            default: null
        }
    }
}
</script>

<template>
  <article class="band-card">
    <div class="image-wrapper">
        <img :src="data.photo_url" :alt="`${data.name} headshot`" />
    </div>
    <div class="content">
        <h3>{{data.name}}</h3>
        <p class="instruments">{{ data.subtitle }}</p>
        <p class="bio">{{ data.bio}}</p>
    </div>
  </article>
</template>

<style lang="scss" scoped>
.band-card {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: $spacing-48;
    flex-wrap: nowrap;
    margin-bottom: $spacing-48;

    @media (max-width: $breakpoint-md) {
        flex-wrap: wrap;
    }

    .image-wrapper {
        flex: 1 0 50%;
        position: relative;
        width: 100% !important;
        max-width: 430px;

        img {
            width: 100%;
        }
    }

    .content {
        flex: 1 0 50%;
        text-align: left;

        h3 {
            font-size: text-heading-3;
            font-weight: $font-weight-bold;
            margin-top: 0;
            margin-bottom: $spacing-24;
        }

        .instruments {
            text-transform: uppercase;
            color: $color-text-100;
            font-size: 14px;
            line-height: 14px;
            margin-bottom: $spacing-24;
        }

        .bio {
            font-size: $text-body-2;
            line-height: $line-height-body-2;
        }
    }
}
</style>