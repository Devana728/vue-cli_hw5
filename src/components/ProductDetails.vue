<template>
    <div>
      <p>name {{ product.name }}</p>
      <p> price {{ formattedPrice }}</p>
      <p v-if="product.available">Available</p>
      <p v-else>Out of stock</p>
    </div>
</template>

<script>

export default {
   name: 'ProductDetails',
    
   data() {
    return {
      product: 
        { 
            name: 'Product-1', 
            price: 99.99,
            available: true, 
        },
    };
  },
  computed: {
    formattedPrice: function() {
        return`$${this.product.price}`;
    }
  }
}
</script>


<style scoped>

</style>