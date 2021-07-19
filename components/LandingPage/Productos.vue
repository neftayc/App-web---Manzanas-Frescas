<template>
  <section id="productos" class="pt-16">
    <v-container class="px-0" fluid>
      <section-title title="Productos Destacados" />
      <VueSlickCarousel v-bind="settings">
        <div v-for="(item, i) in products" :key="i">
          <div class="px-4">
            <card-product
              :image="item.image"
              :title="item.title"
              size-font="text-caption text-xl-subtitle-2"
            />
          </div>
        </div>
        <template #prevArrow="arrowOption">
          <div class="custom-arrow-prev">
            {{ arrowOption.currentSlide }}/{{ arrowOption.slideCount }}
          </div>
        </template>
        <template #nextArrow="arrowOption">
          <div class="custom-arrow-next">
            {{ arrowOption.currentSlide }}/{{ arrowOption.slideCount }}
          </div>
        </template>
      </VueSlickCarousel>
    </v-container>
  </section>
</template>

<script>
import CardProduct from '@/components/UI/CardProduct'
export default {
  components: { CardProduct },
  data: () => ({
    settings: {
      focusOnSelect: true,
      infinite: true,
      slidesToScroll: 1,
      speed: 500,
      autoplay: true,
      initialSlide: 0,
      slidesToShow: 6,
      responsive: [
        {
          breakpoint: 3200,
          settings: {
            slidesToShow: 6,
            slidesToScroll: 1,
            initialSlide: 0,
            infinite: true,
            dots: true,
          },
        },
        {
          breakpoint: 1920,
          settings: {
            slidesToShow: 6,
            slidesToScroll: 1,
            initialSlide: 0,
            infinite: true,
            dots: true,
          },
        },
        {
          breakpoint: 1464,
          settings: {
            slidesToShow: 5,
            slidesToScroll: 1,
            initialSlide: 0,
            infinite: true,
            dots: true,
          },
        },
        {
          breakpoint: 1264,
          settings: {
            slidesToShow: 4,
            slidesToScroll: 1,
            initialSlide: 0,
            infinite: true,
            dots: true,
          },
        },
        {
          breakpoint: 960,
          settings: {
            slidesToShow: 3,
            slidesToScroll: 1,
            initialSlide: 0,
            infinite: true,
            dots: true,
          },
        },
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
    products: [
      {
        image: require('@/assets/images/products/pink-apple-1kg.jpg'),
        title: 'Pink Apple 1 Kg',
      },
      {
        image: require('@/assets/images/products/lal-ambri.jpg'),
        title: 'Lal Ambri 1 Kg',
      },
      {
        image: require('@/assets/images/products/red-apple-1kg.jpg'),
        title: 'Red Delicious Apple 1 Kg',
      },
      {
        image: require('@/assets/images/products/half-red.jpg'),
        title: 'Half Kg Red Delicious Apple',
      },
      {
        image: require('@/assets/images/products/golden-apple-1k.jpg'),
        title: 'Golden Delicious Apple 1 Kg',
      },
      {
        image: require('@/assets/images/products/half-golde-apple.jpg'),
        title: 'Half Kg Golden Delicious Apple',
      },
      {
        image: require('@/assets/images/products/pink-apple-1kg.jpg'),
        title: 'Pink Apple 1 Kg',
      },
    ],
  }),
}
</script>
<style lang="scss" scoped>
.custom-arrow-prev {
  left: 15px;
  z-index: 100;
  &::before {
    font-size: 2rem;
    color: black;
  }
}
.custom-arrow-next {
  right: 28px;
  z-index: 0;
  &::before {
    font-size: 2rem;
    color: black;
  }
}
</style>
