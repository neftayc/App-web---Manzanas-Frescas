<template>
  <section>
    <v-responsive :aspect-ratio="$vuetify.breakpoint.mdAndUp ? 16 / 6 : 16 / 9">
      <v-img
        height="100%"
        :src="require('@/assets/images/main-banner.webp')"
        gradient="to bottom right, rgba(0,0,0,0), rgba(0,0,0,.3)"
      >
        <v-container class="fill-height">
          <v-row align="end">
            <v-col
              cols="12"
              md="9"
              offset-md="3"
              lg="8"
              offset-lg="4"
              xl="7"
              offset-xl="5"
              class="d-flex align-end justify-center"
            >
              <div class="text-center">
                <h2
                  class="text-h6 text-md-h5 text-lg-h4 font-weight-medium mb-1"
                >
                  Disfrute las variedades de
                </h2>
                <h1
                  class="
                    text-h5 text-md-h4 text-lg-h3
                    font-weight-bold
                    mb-5 mb-md-8 mb-lg-10
                  "
                  style="text-shadow: 0 3px 5px black"
                >
                  Manzanas orgánicas de nuestro rico Challabamba
                </h1>
                <v-btn
                  class="
                    text-none
                    font-weight-medium
                    text-subtitle-2 text-sm-subtitle-1
                    px-lg-10
                  "
                  depressed
                  :large="$vuetify.breakpoint.lgAndUp"
                  color="accent"
                >
                  Contactenos
                </v-btn>
              </div>
            </v-col>
          </v-row>
        </v-container>
      </v-img>
    </v-responsive>
  </section>
</template>
<script>
export default {}
</script>
