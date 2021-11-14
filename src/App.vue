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
      cart: [],
      premium: true,
    };
  },
  methods: {
    updateCart(id) {
      this.cart.push(id);
    },
    removeFromCart() {
      if (this.cart) this.cart--;
    },
  },
};
</script>
