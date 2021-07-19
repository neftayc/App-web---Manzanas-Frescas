<template>
  <h2 class="text-center text-h5 text-sm-h4 text-md-h3 pb-8 font-weight-bold">
    {{ title }}
  </h2>
</template>

<script>
export default {
  props: {
    title: { type: String, default: 'Section Title' },
  },
}
</script>
