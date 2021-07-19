<template>
  <div>
    <v-list-item three-line>
      <v-list-item-icon class="mr-5">
        <v-icon color="primary">{{ icon }}</v-icon>
      </v-list-item-icon>
      <v-list-item-content>
        <v-list-item-title class="text-h6 font-weight-light mb-0">
          {{ title }}
        </v-list-item-title>
        <v-list-item-subtitle class="text-caption">
          {{ subtitle }}
        </v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
  </div>
</template>

<script>
export default {
  props: {
    icon: { type: String, default: () => '' },
    title: { type: String, default: () => '' },
    subtitle: { type: String, default: () => '' },
  },
}
</script>
