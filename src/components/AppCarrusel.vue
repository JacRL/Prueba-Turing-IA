<template>
  <div class="container-fluid">
    <!-- Espaciado superior -->
    <div class="clearfix"></div>

    <!-- Barra de navegación -->
    <div class="container-fluid">
      <div class="row">
        <!-- Margen izquierdo -->
        <div class="col-1"></div>

        <!-- Logotipo redondeado -->
        <div class="col-1 rounded text-white">
          <!-- Contenido dentro del div redondeado -->
          <h6 class="text-center">Turing-IA</h6>
        </div>

        <!-- Espacio en blanco -->
        <div class="col-6"></div>

        <!-- Texto a la derecha del div redondeado -->
        <div class="col-1">
          <h6 class="submenu">Texto-1</h6>
        </div>
        <div class="col-1">
          <h6 class="submenu">Texto-2</h6>
        </div>
        <div class="col-1">
          <h6 class="submenu">Texto-3</h6>
        </div>
        <div class="col-1">
          <h6 class="submenu">Texto-4</h6>
        </div>
      </div>
    </div>

    <!-- Espaciado inferior -->
    <div class="clearfix"></div>

    <!-- Contenido del carrusel -->
    <div class="caja_carrusel">
      <!-- Sección de historia, propósito y uso -->
      <div class="container text-center">
        <h6 class="ti-sec-2">HISTORY, PURPOSE AND USAGE</h6>
        <p class="text-white">The purpose of lorem ipsum is to create a natural looking block of text (sentence, paragraph, page, etc.) that doesn't distract from the layout. A practice not without controversy, laying out pages with meaningless filler text can be very useful when the focus is meant to be on design, not content.</p>
      </div>

      <!-- Botón de selección -->
      <div class="container text-center">
        <button class="btn" type="button">
          <p>Selecciona</p><!-- Icono de configuración de Bootstrap -->
        </button>
      </div>

      <!-- Espaciado inferior -->
      <div class="clearfix"></div>

      <!-- Carrusel de imágenes -->
      <div id="myCarousel" class="carousel slide" data-ride="carousel">
        <div class="carousel-inner">
          <!-- Iteración sobre los grupos de elementos -->
          <div v-for="(item, index) in groupedItems" :key="index" :class="{ 'carousel-item': true, 'active': index === 0 }">
            <!-- Creación de filas en el carrusel -->
            <div class="row">
              <!-- Iteración sobre elementos individuales en cada grupo -->
              <div v-for="(subItem, subIndex) in item" :key="subIndex" class="col">
                <!-- Imagenes en el carrusel -->
                <img :src="subItem.link" :alt="subItem.content" class="d-block w-100 h-100">
              </div>
            </div>
          </div>
        </div>
        <!-- Controles de navegación del carrusel -->
        <a class="carousel-control-prev" href="#myCarousel" role="button" data-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="sr-only">Previous</span>
        </a>
        <a class="carousel-control-next" href="#myCarousel" role="button" data-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="sr-only">Next</span>
        </a>
      </div>
    </div>

    <!-- Espaciado inferior -->
    <div class="space"></div>
  </div>
</template>


<script>
export default {
  data() {
    return {
      items: [
        { link: 'https://images.immediate.co.uk/production/volatile/sites/3/2020/11/supernatural-d0c0b62.jpg?quality=90&resize=980,654', content: 'Contenido 1' },
        { link: 'https://media.revistagq.com/photos/60b4a531a091477bf296bfdd/16:9/w_2560%2Cc_limit/LOKI.jpg', content: 'Contenido 2' },
        { link: 'https://media.revistagq.com/photos/5cb72704773e5e65d3fdb3bf/16:9/w_1280,c_limit/series_netflix_2019_1049.jpg', content: 'Contenido 3' },
        { link: 'https://cdn.computerhoy.com/sites/navi.axelspringer.es/public/media/image/2022/02/witcher-2620883.jpg?tf=3840x', content: 'Contenido 4' },
        { link: 'https://occ-0-2794-2219.1.nflxso.net/dnm/api/v6/6AYY37jfdO6hpXcMjf9Yu5cnmO0/AAAABcsNRTCR_xEGk0JKJnrf-zVc7eZYzLh3sojYa1Rude8R_3jboyMRsOysg_b5r0zg69rO15TU_T7aI0lKTy-XVda4em0FsaNpkTcL.jpg?r=15c', content: 'Contenido 5' },
        { link: 'https://cdn.forbes.com.mx/2022/02/the-defenders-640x360.jpg', content: 'Contenido 6' },
        { link: 'https://nosomosnonos.com/wp-content/uploads/2020/07/malcolm-el-de-enmedio.jpeg', content: 'Contenido 7' },
        { link: 'https://cdn.culturagenial.com/es/imagenes/breaking-bad-serie-cke.jpg', content: 'Contenido 8' },
        { link: 'https://media.gq.com.mx/photos/5e5413260c1d83000831ab3d/16:9/w_1280,c_limit/netflix-ya-no-es-bueno-y-por-que-todos-odiaran-streaming.jpg', content: 'Contenido 9' }// Agrega más elementos según sea necesario
      ],
      itemsPerPage: 3,
      activeIndex: 0,
    };
  },
  computed: {
    groupedItems() {
      // Agrupa los elementos de items en grupos de itemsPerPage
      return this.chunkArray(this.items, this.itemsPerPage);
    },
  },
  methods: {
    chunkArray(array, size) {
      // Divide un array en grupos del tamaño especificado
      const chunkedArray = [];
      for (let i = 0; i < array.length; i += size) {
        chunkedArray.push(array.slice(i, i + size));
      }
      return chunkedArray;
    },
    prevSlide() {
      // Mueve a la diapositiva anterior de 3 en 3
      this.activeIndex = Math.max(this.activeIndex - this.itemsPerPage, 0);
    },
    nextSlide() {
      // Mueve a la siguiente diapositiva de 3 en 3
      this.activeIndex = Math.min(this.activeIndex + this.itemsPerPage, this.groupedItems.length - 1);
    },
  },
};
</script>

<style scoped>
.submenu{
  background-color: #CCD8E1;
  width: 100%;
  color: #28B99D;
  text-decoration: underline 2px; /* Añade un subrayado al texto */

}

.container-fluid{
  padding: 5px;
  background: #CCD8E1;
  
}
.space{
  padding: 120px;
    clear: both;
}
.clearfix{
    padding: 8px;
    clear: both;
}

.rounded {
  background-color: #0B2639;
  padding: 10px;
}
.caja_carrusel{
  background-color: #0B2639;
  width: 100%x;
  height: 300px;
  margin: 0 auto; /* Centra el elemento horizontalmente */
  
}
.ti-sec-2{
  padding-top: 40px;
  color: #28B99D !important; 
}
.btn{
  text-align: center;
  color: white;
  background-color: #28B99D;
}
.carousel-inner{
  padding-left: 40px;
  padding-right:40px;
}.btn:hover{
  color: white;
  background-color: #38a58f;
}
/* Puedes agregar estilos adicionales aquí según sea necesario */
</style>
