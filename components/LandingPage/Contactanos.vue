<template>
  <section id="contactos" class="pt-16">
    <v-container>
      <section-title title="Contáctenos" />
      <v-row justify="center">
        <v-col cols="12" sm="6" xl="4">
          <v-card class="pa-2 pa-md-4 fill-height">
            <div class="mb-6">
              <description-item
                icon="mdi-map"
                title="Dirección de nuestra oficina"
                subtitle="CC. Sunchubamba, Challabamba, Paucartambo, Cusco"
              />
            </div>
            <div class="mb-6">
              <description-item
                icon="mdi-message"
                title="Consultas Generales"
                subtitle="rusbel.ccana@example.com"
              />
            </div>
            <div class="mb-6">
              <description-item
                icon="mdi-phone"
                title="Llámanos"
                subtitle="+51 973108795"
              />
            </div>
          </v-card>
        </v-col>
        <v-col cols="12" sm="6" xl="4">
          <v-card class="pa-2 pa-md-4 fill-height">
            <v-text-field outlined placeholder="Nombre"></v-text-field>
            <v-text-field
              outlined
              placeholder="Correo Electrónico"
            ></v-text-field>
            <v-text-field outlined placeholder="Telefono"></v-text-field>
            <v-text-field outlined placeholder="Mensaje"></v-text-field>
            <div class="text-center">
              <v-btn class="text-none px-8" large color="accent">Enviar</v-btn>
            </div>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
import DescriptionItem from '@/components/UI/DescriptionItem'
export default {
  components: { DescriptionItem },
}
</script>
