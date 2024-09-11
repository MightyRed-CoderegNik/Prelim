<template>
  <div class="product-item">
    <img :src="product.image" :alt="product.name" class="product" />
    <h3>{{ product.name }}</h3>
    <p class="product-price">Price: ${{ product.price }}</p>
    <button @click="addToCart">Add To Cart</button>
  </div>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'ProductItem',
  props: {
    product: {
      type: Object,
      required: true,
    },
  },
  methods: {
    addToCart() {
      this.$emit('add-to-cart', this.product); 
    },
  },
});
</script>

<style scoped>
.product-item {
  background-color: white;
  border-radius: 8px;
  padding: 15px;
  text-align: center;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  transition: transform 0.2s ease-in-out;
  max-width: 200px;
  cursor: pointer;
}

.product-item:hover {
  transform: translateY(-5px);
}

.product-item img {
  max-width: 100%;
  border-radius: 8px;
  margin-bottom: 10px;
}

.product-item h3 {
  font-size: 16px;
  color: #333;
  margin-bottom: 10px;
  font-weight: bold;
}

.product-price {
  font-size: 18px;
  color: #ff5722;
  margin: 15px 0;
  font-weight: bold;
}

.product-item button {
  background-color: #007bff;
  color: white;
  border: none;
  padding: 10px 15px;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.product-item button:hover {
  background-color: #0056b3;
}
</style>
