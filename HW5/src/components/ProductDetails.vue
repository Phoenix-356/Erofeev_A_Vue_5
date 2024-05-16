<template>
    <div class="product-details">
      <h1>{{ product.name }}</h1>
      <p>Цена: {{ formattedPrice }}</p>
      <p>Статус: <span v-if="product.available">Available</span><span v-else>Out of stock</span></p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ProductDetails',
    props: {
      product: {
        type: Object,
        required: true
      }
    },
    computed: {
      formattedPrice() {
        return `$${this.product.price.toFixed(2)}`;
      }
    }
  };
  </script>
  
  <style scoped>
  .product-details {
    max-width: 400px;
    margin: auto;
    border: 1px solid #ddd;
    padding: 1em;
    border-radius: 4px;
  }
  
  .product-details h1 {
    font-size: 1.5em;
    margin-bottom: 0.5em;
  }
  
  .product-details p {
    margin: 0.5em 0;
  }
  
  .product-details span {
    font-weight: bold;
  }
  </style>
  