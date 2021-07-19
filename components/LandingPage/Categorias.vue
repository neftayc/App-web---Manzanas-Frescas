<template>
  <section id="categorias" class="pt-16">
    <v-container>
      <section-title title="Categorías" />
      <v-row>
        <v-col v-for="(item, i) in categorias" :key="i" cols="6" md="3">
          <card-product
            :image="item.image"
            :title="item.title"
            size-font="text-subtitle-2 text-sm-body-2 text-md-body-1 font-weight-regular"
          />
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
import CardProduct from '@/components/UI/CardProduct'

export default {
  components: { CardProduct },
  data: () => ({
    categorias: [
      {
        image: require('@/assets/images/red-delicious.webp'),
        title: 'Red Delicious Apples',
        tipo: '',
      },
      {
        image: require('@/assets/images/golden-delicious.webp'),
        title: 'Golden Delicious Apples',
        tipo: '',
      },
      {
        image: require('@/assets/images/pink.webp'),
        title: 'Pink Apples',
        tipo: '',
      },
      {
        image: require('@/assets/images/lal-ambri.webp'),
        title: 'Lal Ambri',
        tipo: '',
      },
    ],
  }),
}
</script>
