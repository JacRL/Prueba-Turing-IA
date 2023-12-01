<!-- components/AppHeader.vue -->
<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
      <div class="container-fluid">
        
        <a class="navbar-brand" href="#">Prueba-Practicas</a>
        <div></div>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item ">          
              <router-link to="#" class="nav-link rounded">Servicios</router-link>           
            </li>
             <li class="nav-item">                
               <router-link to="#" class="nav-link rounded">Contactos</router-link>
            </li>
          </ul>
          <div class="d-flex">
            <button class="btn btn-outline-light" type="button">
              <i class="bi bi-search"></i> <!-- Icono de configuración de Bootstrap -->
            </button>
            <button class="btn btn-outline-light" type="button">
              <i class="bi bi-gear"></i> <!-- Icono de configuración de Bootstrap -->
            </button>
            <button class="btn btn-outline-light" type="button">
              <i class="bi bi-bell"></i> <!-- Icono de configuración de Bootstrap -->
            </button>
          </div>
        </div>
      </div>
    </nav>
    <router-view></router-view>
  </div>
</template>

<style scoped>
.contenedor {
  height: 100%;
  width: 100%;
  display: flex;
  position: fixed;
  align-items: center;
  justify-content: center;
  color: antiquewhite;
}

.navbar {
  background-color: #0B2639 !important;        
}
/* Agrega estilos para el hover de los botones */
.navbar-nav .nav-item .nav-link:hover {
  background-color: #28B99D !important; /* Puedes ajustar el color azul según tu preferencia */
  color: white !important; /* Puedes ajustar el color del texto cuando se hace hover */
}
/* Agrega estilos para el hover de los iconos */
.d-flex button:hover i {
  color: #28B99D !important;
}
</style>
