<!-- views/App.vue -->
<template>
  <div>
    <AppHeader />
    <AppCarrusel />
    <AppContent />
    <AppSection4 />
    <AppFooter />
  </div>
</template>

<script>
import AppHeader from '@/components/AppHeader.vue';
import AppCarrusel from '@/components/AppCarrusel.vue';
import AppContent from '@/components/AppContent.vue';
import AppSection4 from '@/components/AppSection4.vue';
import AppFooter from '@/components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    AppCarrusel,
    AppContent,
    AppSection4,
    AppFooter,
  },
};
</script>

<style scoped>
/* Puedes agregar estilos adicionales aquí según sea necesario */
body {
  padding-top: 56px; /* Ajusta según la altura de tu barra de navegación */
}
</style>
