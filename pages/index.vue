<template>
  <div id="inicio">
    <!-- Section Banner -->
    <banner />
    <!-- Section Categorias -->
    <categorias />
    <!-- Section Productos -->
    <productos />
    <!-- Section Nosotros -->
    <nosotros />
    <!-- Section Galeria -->
    <galeria />
    <!-- Section Testimonios -->
    <testimonios />
    <!-- Section Contactanos -->
    <contactanos />
    <!-- Section Mapa -->
    <mapa />
  </div>
</template>
<script>
import Banner from '@/components/LandingPage/Banner'
import Categorias from '@/components/LandingPage/Categorias'
import Productos from '~/components/LandingPage/Productos'
import Nosotros from '~/components/LandingPage/Nosotros'
import Galeria from '~/components/LandingPage/Galeria'
import Testimonios from '~/components/LandingPage/Testimonios'
import Contactanos from '~/components/LandingPage/Contactanos'
import Mapa from '~/components/LandingPage/Mapa'
export default {
  components: {
    Banner,
    Categorias,
    Productos,
    Nosotros,
    Galeria,
    Testimonios,
    Contactanos,
    Mapa,
  },
}
</script>
