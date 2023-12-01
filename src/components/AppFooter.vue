<!-- components/AppFooter.vue -->
<template>

<footer class="bgcolor text-center text-lg-start text-white">
  <!-- Grid container -->
  <div class="container p-4">
    <!--Grid row-->
    <div class="row mt-4">
      <!--Grid column-->
      <div class="col-lg-3 col-md-6 mb-4 mb-md-0">
        <div class="d-flex">
            <!-- Contenido del div centrado -->
            <div v-for="index in 3" :key="index + 4" class="circle"></div>
          </div>
        <div class="col-lg-3 col-md-6 mb-4 mb-md-0">
          <ul class="list-unstyled mb-0">
            <li>
              <a href="#!" class="text-white">Bestsellers</a>
            </li>
            <li>
              <a href="#!" class="text-white">All books</a>
            </li>
            <li>
              <a href="#!" class="text-white">Our authors</a>
            </li>
          </ul>
      </div>
      </div>
      <!--Grid column-->

      <!--Grid column-->
      <div class="col-lg-3 col-md-6 mb-4 mb-md-0">
        <h5 class="text-uppercase">Execution of the contract</h5>

        <ul class="list-unstyled">
          <li>
            <a href="#!" class="text-white"><i class="fas fa-shipping-fast fa-fw fa-sm me-2"></i>Supply</a>
          </li>
          <li>
            <a href="#!" class="text-white"><i class="fas fa-backspace fa-fw fa-sm me-2"></i>Returns</a>
          </li>
          <li>
            <a href="#!" class="text-white"><i class="far fa-file-alt fa-fw fa-sm me-2"></i>Regulations</a>
          </li>
          <li>
            <a href="#!" class="text-white"><i class="far fa-file-alt fa-fw fa-sm me-2"></i>Privacy policy</a>
          </li>
        </ul>
      </div>
      <!--Grid column-->

      <!--Grid column-->
      <div class="col-lg-3 col-md-6 mb-4 mb-md-0">
        <h5 class="text-uppercase">Publishing house</h5>

        <ul class="list-unstyled">
          <li>
            <a href="#!" class="text-white">The BookStore</a>
          </li>
          <li>
            <a href="#!" class="text-white">123 Street</a>
          </li>
          <li>
            <a href="#!" class="text-white">05765 NY</a>
          </li>
          <li>
            <a href="#!" class="text-white">Send us a book</a>
          </li>
        </ul>
      </div>
      <!--Grid column-->

      <!--Grid column-->
      <div class="col-lg-3 col-md-6 mb-4 mb-md-0">
        <h5 class="text-uppercase">Write to us</h5>

        <ul class="list-unstyled">
          <li>
            <a href="#!" class="text-white"><i class="fas fa-at fa-fw fa-sm me-2"></i>Help in purchasing</a>
          </li>
          <li>
            <a href="#!" class="text-white"><i class="fas fa-shipping-fast fa-fw fa-sm me-2"></i>Check the order status</a>
          </li>
          <li>
            <a href="#!" class="text-white"><i class="fas fa-envelope fa-fw fa-sm me-2"></i>Join the newsletter</a>
          </li>
        </ul>
      </div>
      <!--Grid column-->
    </div>
    <!--Grid row-->
  </div>
  <!-- Grid container -->

  <!-- Copyright -->
  <div class="text-center p-3" style="background-color: rgba(0, 0, 0, 0.2)">
    © 2023 Copyright Jose Jacob RL
  </div>
  <!-- Copyright -->
</footer>

<!-- End of .container -->
</template>

<script>
export default {
  // ... tu código existente ...
};
</script>

<style scoped>
.bgcolor{
  background-color: #0B2639;
}
.text-uppercase{
  color: #28B99D;
}
.circle{
  background-color: #28B99D;
  width: 30px;
  height: 30px;
  border-radius: 50%;
  margin-right: 10px;
}
</style>
