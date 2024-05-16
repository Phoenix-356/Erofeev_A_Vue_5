<template>
    <div class="product-list">
      <ProductDetails v-for="product in products" :key="product.id" :product="product" />
    </div>
  </template>
  
  <script>
  import ProductDetails from './ProductDetails.vue';
  
  export default {
    name: 'ProductList',
    components: {
      ProductDetails
    },
    data() {
      return {
        products: [
          { id: 1, name: 'Пример продукта 1', price: 99.99, available: true },
          { id: 2, name: 'Пример продукта 2', price: 149.99, available: false },
          { id: 3, name: 'Пример продукта 3', price: 199.99, available: true },
          { id: 4, name: 'Пример продукта 4', price: 249.99, available: false }
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  .product-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
  }
  </style>
  