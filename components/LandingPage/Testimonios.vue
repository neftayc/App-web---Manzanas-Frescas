<template>
  <section id="testimonios" class="pt-16">
    <v-parallax
      :height="$vuetify.breakpoint.mdAndUp ? 560 : 380"
      :src="require('@/assets/images/banner-testimonial.webp')"
    >
      <section-title title="Testimonios" class="pt-12 primary--text" />
      <v-avatar size="54" tile class="mx-auto">
        <v-img
          contain
          height="100%"
          :src="require('@/assets/images/icon.webp')"
        ></v-img>
      </v-avatar>
      <v-container class="fill-height">
        <v-carousel
          cycle
          :show-arrows="false"
          hide-delimiter-background
          dark
          height="100%"
          class="main-carousel"
        >
          <v-carousel-item v-for="(slide, i) in testimonios" :key="i">
            <v-card
              flat
              tile
              class="transparent text-center mx-auto"
              :max-width="$vuetify.breakpoint.mdAndUp ? '80%' : ''"
            >
              <v-card-text
                class="
                  text-subtitle-1 text-md-h6
                  font-weight-regular
                  black--text
                  pb-0
                "
              >
                {{ slide.description }}
              </v-card-text>
              <v-card-title
                class="
                  text-h6 text-md-h5
                  black--text
                  font-weight-bold
                  pt-0
                  justify-center
                  text-center
                "
              >
                {{ slide.user }}
              </v-card-title>
            </v-card>
          </v-carousel-item>
        </v-carousel>
      </v-container>
    </v-parallax>
  </section>
</template>

<script>
export default {
  data: () => ({
    testimonios: [
      {
        description:
          'This was the first time I ordered apples online. I have no complaints from them.',
        user: 'Rosesh Roy',
      },
      {
        description:
          'This was the first time I ordered apples online. I have no complaints from them.',
        user: 'Neftali Ccana',
      },
      {
        description:
          'This was the first time I ordered apples online. I have no complaints from them.',
        user: 'Rusbel Yucra',
      },
    ],
  }),
}
</script>
<style lang="scss">
.main-carousel {
  .v-carousel__controls {
    .v-carousel__controls__item {
      color: var(--primary-color) !important;
      &.v-btn--active {
        color: var(--primary-color) !important;
      }
    }
  }
}
</style>
