<template>
    <div class="fondo pt-5">
      <div class="text-center mt-1 mb-5">
        <h6 class="encab">SECCION-4</h6>
      </div>
      <div class="container-fluid seccion4">
        <div class="caja2 rounded" v-for="index in 3" :key="index + 4">
          <!-- Contenido del div centrado -->
          <div class="circle"></div>
          <div class="ab_caja rounded">
            <p>Lorem ipsum dolor sit amet</p>
          </div>
          <div class="ab_caja rounded">
            <p>is simply dummy text </p>
          </div>
          <div class="ab_caja2 rounded">
            <p>Lorem ipsum</p>
          </div>
          
        </div>
      </div>
    </div>
  </template>
  
  <style scoped>
  .fondo {
    background-color: #CCD8E1;
    padding: 10px; /* Ajuste del espacio interno */
    height: 100%;
    margin: auto;
  }
  
  .container-fluid {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    align-items: center;
    background-color: #CCD8E1;
  }
  
  .seccion4 {
    height: 100%;
    margin-bottom: 20px; /* Ajuste del margen inferior para separar del fondo */
  }
  
  .circle {
    width: 250px;
    height: 250px;
    margin-top: 20px; /* Ajuste del margen superior para separar del elemento anterior */
    background-color: #0B2639;
    border-radius: 50%;
  }
  .encab {
  color: #28B99D !important;
  font-weight: bold;
}
.ab_caja {
  width: 100%;
  height: 20px;
  text-align: center;
  color: #0B2639;
  font-weight: bold;
}
.ab_caja2 {
  width: 100%;
  height: 20px;
  text-align: center;
  color: #28B99D;
  font-weight: bold;
}
  /* ... (resto de estilos) ... */
  </style>
  