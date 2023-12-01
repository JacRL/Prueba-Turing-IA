<template>
  <!-- Contenedor principal -->
  <div class="fondo">
    <!-- Sección 2 -->
    <div class="text-center">
      <h6 class="encab">SECCION-2</h6>
    </div>

    <!-- Contenedor fluido para cajas -->
    <div class="container-fluid">
      <!-- Iteración para la primera serie de cajas -->
      <div class="box rounded" v-for="index in 3" :key="index">
        <!-- Contenido del div centrado -->
        <div class="content">
          <!-- Caja interna -->
          <div class="inner-box"></div>
          <!-- Párrafo de texto -->
          <p class="texto">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
          <!-- Caja adicional -->
          <div class="ab_caja rounded">
            <p>Lorem ipsum dolor sit amet</p>
          </div>
        </div>
      </div>

      <!-- Iteración para la segunda serie de cajas -->
      <div class="box rounded" v-for="index in 3" :key="index + 3">
        <div class="content">
          <div class="inner-box"></div>
          <p class="texto">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
          <div class="ab_caja rounded">
            <p>Lorem ipsum dolor sit amet</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Sección 3 -->
    <div class="text-center">
      <h6 class="encab2">SECCION-3</h6>
    </div>

    <!-- Contenedor fluido para cuadros -->
    <div class="container-fluid">
      <!-- Iteración para la serie de cuadros -->
      <div class="caja2 rounded" v-for="index in 4" :key="index">
        <!-- Contenido del cuadro -->
        <div class="cuadro2"></div>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: 'CentradosConContenidoComponent',
};
</script>

<style scoped>

.fondo {
  background-color: #CCD8E1;
  padding: 10px; /* Ajuste del espacio interno */
  height: 120%;
  margin: auto;
}

.container-fluid {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  background-color: #CCD8E1;
}

.encab {
  color: #28B99D !important;
  font-weight: bold;
}
.encab2 {
  color: #28B99D !important;
  font-weight: bold;
  margin-top: 60px;
}
.ab_caja {
  width: 100%;
  height: 20px;
  border-top: #0B2639 solid 1px;
  text-align: center;
  color: #28B99D;
  font-weight: bold;
}
.caja2 {
  width: 280px;
  height: 250px;
  margin-top: 100px;
}
.circle {
  width: 250px;
  height: 250px;
  margin-top: 100px;
  background-color: #0B2639;
  border-radius: 50%;
}
.caja3 {
  width: 280px;
  height: 250px;
  margin-top: 100px;
}

.box {
  width: 25%;
  height: 300px;
  border: 1px solid #0B2639;
  margin-left: 10px;
  margin-right: 10px;
  margin-top: 50px;
}
.cuadro2 {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  height: 100%;
  background-color: #28B99D;
}
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  height: 100%;
}

.texto {
  justify-content: center;
  text-align: justify;
  padding: 10px;
}

.inner-box {
  width: 80%;
  height: 60px;
  background-color: #0B2639;
  margin-top: 10px;
  text-align: center;
}

</style>
