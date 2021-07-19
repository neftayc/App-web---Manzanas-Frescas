<template>
  <section id="galeria" class="pt-16">
    <v-container>
      <section-title title="Galeria" />
      <v-row v-if="$vuetify.breakpoint.mdAndUp">
        <v-col v-for="(item, i) in images" :key="i" cols="6" sm="4" xl="3">
          <v-card><v-img :src="item.image"></v-img></v-card>
        </v-col>
      </v-row>

      <VueSlickCarousel v-else v-bind="settings">
        <div v-for="(item, i) in images" :key="i">
          <div class="px-4">
            <v-card><v-img :src="item.image"></v-img></v-card>
          </div>
        </div>
        <template #prevArrow="arrowOption">
          <div class="custom-arrow-gallery-prev">
            {{ arrowOption.currentSlide }}/{{ arrowOption.slideCount }}
          </div>
        </template>
        <template #nextArrow="arrowOption">
          <div class="custom-arrow-gallery-next">
            {{ arrowOption.currentSlide }}/{{ arrowOption.slideCount }}
          </div>
        </template>
      </VueSlickCarousel>
    </v-container>
  </section>
</template>

<script>
export default {
  data: () => ({
    images: [
      { title: '', image: require('@/assets/images/galerias/image1.jpg') },
      { title: '', image: require('@/assets/images/galerias/image2.webp') },
      { title: '', image: require('@/assets/images/galerias/image3.webp') },
      { title: '', image: require('@/assets/images/galerias/image3.webp') },
      { title: '', image: require('@/assets/images/galerias/image1.jpg') },
      { title: '', image: require('@/assets/images/galerias/image2.webp') },
      { title: '', image: require('@/assets/images/galerias/image2.webp') },
      { title: '', image: require('@/assets/images/galerias/image3.webp') },
      { title: '', image: require('@/assets/images/galerias/image1.jpg') },
    ],
    settings: {
      focusOnSelect: true,
      infinite: true,
      slidesToScroll: 1,
      speed: 1500,
      autoplay: true,
      initialSlide: 1,
      slidesToShow: 3,
      dots: true,
      responsive: [
        {
          breakpoint: 600,
          settings: {
            slidesToShow: 2,
            slidesToScroll: 1,
            initialSlide: 0,
          },
        },
        {
          breakpoint: 360,
          settings: {
            slidesToShow: 1,
            slidesToScroll: 1,
          },
        },
      ],
    },
  }),
}
</script>
<style lang="scss">
.custom-arrow-gallery-prev {
  left: 15px;
  z-index: 100;
  &::before {
    font-size: 2rem;
    color: black;
  }
}
.custom-arrow-gallery-next {
  right: 28px;
  z-index: 0;
  &::before {
    font-size: 2rem;
    color: black;
  }
}
.slick-dots {
  li {
    button::before {
      color: var(--secondary-color);
      font-size: 1rem;
    }
    &.slick-active button::before {
      color: var(--primary-color);
    }
  }
}
</style>
