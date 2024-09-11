<template>
  <div id="App">
    <ProductList :products="products" />
  </div>
</template>

<script>
import { defineComponent } from 'vue';
import ProductList from '@/components/ProductList.vue';

export default defineComponent({
  name: 'App',
  components: {
    ProductList,
  },
  data() {
    return {
      products: [
        { 
          id: 1, 
          name: 'Jordan', 
          price: 100, 
           
        },
        { 
          id: 2, 
          name: 'Clarkson', 
          price: 500, 
          
        },
        { 
          id: 3, 
          name: 'Jorge', 
          price: 150, 
           
        },
        { 
          id: 3, 
          name: 'Okay', 
          price: 150, 
           
        },
        { 
          id: 3, 
          name: 'Jordan Shoes', 
          price: 100, 
           
        },
        { 
          id: 3, 
          name: 'Puma', 
          price: 200, 
           
        },
      ],
    };
  },
});
</script>

<style scoped>
#app {
  font-family: 'Avenir', Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: #f5f5f5;
  padding: 20px;
}
</style>
