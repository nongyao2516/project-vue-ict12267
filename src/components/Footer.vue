<template >
    <div class="footer" v-if="!isLoginPage">




<!-- Footer -->
<footer class="bg-dark text-white py-4 mt-auto">
    <div class="container">
        <div class="row">
            <!-- Company Info -->
            <div class="col-md-4 mb-3">
                <h5>About Us</h5>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vel magna elit.</p>
            </div>

            <!-- Links -->
            <div class="col-md-4 mb-3">
                <h5>Quick Links</h5>
                <ul class="list-unstyled">
                    <li><a href="#" class="text-white text-decoration-none">Home</a></li>
                    <li><a href="#" class="text-white text-decoration-none">Products</a></li>
                    <li><a href="#" class="text-white text-decoration-none">Services</a></li>
                    <li><a href="#" class="text-white text-decoration-none">Contact Us</a></li>
                </ul>
            </div>

            <!-- Social Media Links -->
            <div class="col-md-4 mb-3">
                <h5>Follow Us</h5>
                <a href="https://www.facebook.com" target="_blank" class="text-white me-3">
                    <i class="bi bi-facebook"></i>
                </a>
                <a href="https://line.me" target="_blank" class="text-white me-3">
                    <i class="bi bi-line"></i>
                </a>
                <a href="https://twitter.com" target="_blank" class="text-white me-3">
                    <i class="bi bi-twitter"></i>
                </a>
                <a href="https://instagram.com" target="_blank" class="text-white">
                    <i class="bi bi-instagram"></i>
                </a>
            </div>
        </div>

        <!-- Footer Bottom -->
        <div class="text-center mt-3">
            <p class="mb-0">&copy; 2024 Your Company. All Rights Reserved.</p>
        </div>
    </div>
</footer>

</div>




</template>
<script>
import { computed } from 'vue'
import { useRoute } from 'vue-router'

export default {
   name: 'footer',

   setup() {
    const route = useRoute()
    
    // ตรวจสอบว่า route ปัจจุบันเป็น 'Login' หรือไม่
    const isLoginPage = computed(() => route.name === 'login')
    
    return { isLoginPage }
   }
}
</script>
