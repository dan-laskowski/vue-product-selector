<template>
  <Product :premium="premium" :cart="cart" @add-to-cart="updateCart" />
</template>

<script>
import Product from './components/Product.vue';

export default {
  name: 'App',

  components: {
    Product,
  },
  data() {
    return {
      cart: 0,
      premium: true,
    };
  },
  methods: {
    updateCart() {
      this.cart++;
    },
    removeFromCart() {
      if (this.cart) this.cart--;
    },
  },
};
</script>
