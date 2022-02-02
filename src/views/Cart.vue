<template>
  <div>
    <h1>Your Cart</h1>
    <CartItemCard
      v-for="product in products"
      :key="product.id"
      :product="product"
    />
    <CartSummeryPaymentCard :products="products" />
  </div>
</template>

<script>
import CartItemCard from "../components/cart/CartItemCard.vue";
import CartSummeryPaymentCard from "../components/cart/CartSummeryPaymentCard.vue";

export default {
  components: {
    CartItemCard,
    CartSummeryPaymentCard,
  },
  computed: {
    products() {
      return this.$store.getters.cartItems;
    },
  },
};
</script>
