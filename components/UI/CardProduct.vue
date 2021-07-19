<template>
  <v-card class="fill-height d-flex flex-column justify-space-between">
    <v-img :src="image"></v-img>
    <v-card-title class="justify-center text-center" :class="sizeFont">
      <v-list-item-title>{{ title }}</v-list-item-title>
    </v-card-title>
  </v-card>
</template>

<script>
export default {
  props: {
    sizeFont: { type: String, require: true, default: () => '' },
    image: { type: String, require: true, default: () => '' },
    title: { type: String, require: true, default: () => '' },
  },
}
</script>
