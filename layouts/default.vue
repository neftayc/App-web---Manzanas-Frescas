<template>
  <v-app dark>
    <v-app-bar fixed app color="primary" class="menu-desktop">
      <v-toolbar-title class="font-weight-bold" v-text="title" />
      <v-spacer />
      <template v-if="$vuetify.breakpoint.lgAndUp">
        <v-btn
          v-for="item in items"
          :key="item.title"
          text
          :href="`#${item.to}`"
          class="text-none font-weight-light font-weight-default"
        >
          {{ item.title }}
        </v-btn>
      </template>
      <v-menu :close-on-content-click="false" offset-y max-width="320">
        <template #activator="{ on, attrs }">
          <v-avatar size="38" class="ml-3" v-bind="attrs" v-on="on">
            <v-img src="https://cdn.vuetifyjs.com/images/john.jpg"></v-img>
          </v-avatar>
        </template>

        <v-card>
          <v-list>
            <v-list-item>
              <v-list-item-avatar>
                <img
                  src="https://cdn.vuetifyjs.com/images/john.jpg"
                  alt="John"
                />
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title>Rusbel Neftali Ccana</v-list-item-title>
                <v-list-item-subtitle>
                  Fundador de Sparrow Group - Tecnology
                </v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
          </v-list>

          <v-divider></v-divider>

          <v-list>
            <v-list-item>
              <v-list-item-action>
                <v-switch color="purple"></v-switch>
              </v-list-item-action>
              <v-list-item-title>Pedidos</v-list-item-title>
            </v-list-item>

            <v-list-item>
              <v-list-item-action>
                <v-switch color="purple"></v-switch>
              </v-list-item-action>
              <v-list-item-title>Perfil</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-card>
      </v-menu>
    </v-app-bar>
    <v-main class="pb-8">
      <Nuxt />
      <v-btn fab fixed bottom right class="mb-12 mr-n3" color="accent">
        <v-icon>mdi-cart-plus</v-icon>
      </v-btn>
    </v-main>
    <v-footer class="text-center justify-center py-8">
      <span>Sparrow Group &copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
    <v-bottom-navigation
      v-if="$vuetify.breakpoint.mdAndDown"
      v-model="value"
      fixed
      color="primary"
      app
    >
      <v-btn
        v-for="item in items"
        :key="item.to"
        :value="item.to"
        :href="`#${item.to}`"
      >
        <span class="text-center text-caption">{{ item.title }}</span>
        <v-icon>{{ item.icon }}</v-icon>
      </v-btn>
    </v-bottom-navigation>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    value: 'recent',
    items: [
      {
        icon: 'mdi-home',
        title: 'Inicio',
        to: 'inicio',
      },
      {
        icon: 'mdi-shape',
        title: 'Categoría',
        to: 'categorias',
      },
      {
        icon: 'mdi-account-multiple-check-outline',
        title: 'Nosotros',
        to: 'nosotros',
      },
      {
        icon: 'mdi-image-search',
        title: 'Galería',
        to: 'galeria',
      },
      {
        icon: 'mdi-phone-in-talk',
        title: 'Contactos',
        to: 'contactos',
      },
    ],
    title: 'Manzanas Frescas',
  }),
}
</script>

<style lang="scss">
.menu-desktop {
  box-shadow: 0 2px 4px -1px #79a27fad, 0 4px 5px 0 rgb(47 183 109 / 14%),
    0 1px 10px 0 rgb(0 0 0 / 12%) !important;
}
</style>
