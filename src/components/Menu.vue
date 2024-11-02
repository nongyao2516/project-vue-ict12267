<template >
<div id = "nav" v-if="!isLoginPage" >
<nav class="navbar navbar-expand-lg bg-primary-subtle">
  <div class="container">
    <a class="navbar-brand" href="#">DD Shop</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarScroll" aria-controls="navbarScroll" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarScroll">
      <ul class="navbar-nav me-auto my-2 my-lg-0 navbar-nav-scroll" style="--bs-scroll-height: 100px;">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="/">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/product">Product</a>
        </li>
         <li class="nav-item">
          <a class="nav-link" href="/show_product">Show_Product</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/about">About</a>
        </li>
         <li class="nav-item">
          <a class="nav-link" href="/contact">Contact</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/form">Add Products</a>
        </li>
        <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            Register
          </a>
          <ul class="dropdown-menu">
            <li><a class="dropdown-item" href="#">Register</a></li>
            <li><a class="dropdown-item" href="/login">Login</a></li>
            <li><hr class="dropdown-divider"></li>
            <li><a class="dropdown-item" href="#">Logout</a></li>
          </ul>
        </li>
        
      </ul>
      <form class="d-flex" role="search">
        <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
        <button class="btn btn-outline-success" type="submit">Search</button>
      </form>
    </div>
  </div>
</nav>

</div>

</template>

<script>
import { computed } from 'vue'
import { useRoute } from 'vue-router'


export default {
    name: 'Menu',

    setup() {
    const route = useRoute()
    
    // ตรวจสอบว่า route ปัจจุบันเป็น 'Login' หรือไม่
    const isLoginPage = computed(() => route.name === 'login')
    
    return { isLoginPage }
  }


}
</script>

