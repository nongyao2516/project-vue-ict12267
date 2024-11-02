
<template>
  <div>
    <h2>รายการสินค้า:</h2>
    <ul>
      <li v-for="(product, index) in products" :key="index">
        {{ index + 1 }}. {{ product.name }} จำนวน {{ product.num }} ชิ้น - ราคา: {{ product.price }}บาท เป็นเงิน {{ product.price * product.num }} บาท
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      products: [
        { name: 'สินค้า 1', price: 100, num: 2 },
        { name: 'สินค้า 2', price: 200, num: 5  },
        { name: 'สินค้า 3', price: 300, num: 3  },
      ], // อาร์เรย์เก็บรายการสินค้า
    };
  },
};
</script>

