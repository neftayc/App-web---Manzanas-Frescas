<template>
  <section id="nosotros" class="pt-16">
    <v-card elevation="8" tile>
      <v-container>
        <v-row justify="center" align="center">
          <v-col cols="12" sm="10" md="8" lg="7" class="text-center">
            <section-title title="Sobre Nosotros" />
            <v-avatar
              v-if="$vuetify.breakpoint.smAndDown"
              size="180"
              class="mx-auto text-center"
            >
              <v-img :src="require('@/assets/images/about-image.webp')"></v-img>
            </v-avatar>
            <p
              class="
                text-body-1 text-md-h6
                font-weight-light
                text-center text-md-left
              "
            >
              We, Amar, situated at Malad West, Mumbai, Maharashtra are
              internationally reputed computer training and interior designing
              institute in Mumbai. Our main focus is on orienting students to
              develop creativity & provide personalized career counselling that
              helps to ensure that they stay on track for a successful career.
              We aim to provide world class learning environment using latest
              software. We are proud to have one of the best setup in the
              industry. Our creative approach grooms students through strong
              academics and practical real world experiences. Our classrooms are
              designed to bring the best from our students by nurturing their
              creativity, confidence and making them the future leaders of the
              industry.
            </p>
          </v-col>
          <v-col v-if="$vuetify.breakpoint.mdAndUp" cols="12" md="4" lg="5">
            <v-card flat tile max-width="500" class="mx-auto transparent">
              <v-img :src="require('@/assets/images/about-image.webp')"></v-img>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-card>
  </section>
</template>

<script>
export default {}
</script>
