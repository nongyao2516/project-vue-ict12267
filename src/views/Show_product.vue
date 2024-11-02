<template lang="">
<div class="show_product"> 

<div class="container my-5">
    <h1>Product Catalog</h1>
    <div class="row" id="productList">
        <!-- Product 1 -->
        <div class="col-md-3 mb-4">
            <div class="card">
                <img src="https://via.placeholder.com/150" class="card-img-top" alt="Product 1">
                <div class="card-body">
                    <h5 class="card-title">Product 1</h5>
                    <p class="card-text">$10.00</p>
                    <button class="btn btn-primary add-to-cart" data-name="Product 1" data-price="10.00">Add to Cart</button>
                </div>
            </div>
        </div>
        <!-- Product 2 -->
        <div class="col-md-3 mb-4">
            <div class="card">
                <img src="https://via.placeholder.com/150" class="card-img-top" alt="Product 2">
                <div class="card-body">
                    <h5 class="card-title">Product 2</h5>
                    <p class="card-text">$20.00</p>
                    <button class="btn btn-primary add-to-cart" data-name="Product 2" data-price="20.00">Add to Cart</button>
                </div>
            </div>
        </div>
        <!-- Add more products here -->
    </div>

    <h2 class="mt-5">Shopping Cart</h2>
    <ul id="cartItems" class="list-group mb-3"></ul>
    <p><strong>Total:</strong> $<span id="cartTotal">0.00</span></p>
</div>







</div>
</template>

<script>
    const cartItems = [];
    const cartItemsList = document.getElementById('cartItems');
    const cartTotal = document.getElementById('cartTotal');

    // Function to add items to the cart
    function addToCart(name, price) {
        // Add item to cart array
        cartItems.push({ name, price });
        displayCartItems();
    }

    // Function to display cart items and total price
    function displayCartItems() {
        // Clear current cart items display
        cartItemsList.innerHTML = '';
        let total = 0;

        // Display each item in the cart
        cartItems.forEach(item => {
            const listItem = document.createElement('li');
            listItem.className = 'list-group-item';
            listItem.textContent = `${item.name} - $${item.price}`;
            cartItemsList.appendChild(listItem);
            total += parseFloat(item.price);
        });

        // Update total price
        cartTotal.textContent = total.toFixed(2);
    }

    // Add event listeners to all "Add to Cart" buttons
    document.querySelectorAll('.add-to-cart').forEach(button => {
        button.addEventListener('click', () => {
            const name = button.getAttribute('data-name');
            const price = button.getAttribute('data-price');
            addToCart(name, price);
        });
    });
</script>
