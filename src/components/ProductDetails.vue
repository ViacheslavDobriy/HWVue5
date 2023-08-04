<template>
  <div class="product">
    <h1 class="product__name">{{ product.name }}</h1>
    <h2 class="product__price">Цена товара {{ formattedPrice }}</h2>
    <h2 class="product__available"> {{ availability }}</h2>
  </div>
</template>

<script>
export default {
  name: 'ProductDetails',
  data() {
    return {
      product: {
        name: 'Shoe',
        price: 99.99,
        isAvailable: false
      }
    }
  },
  computed: {
    formattedPrice: function() { return '$' + this.product.price;},
    availability() {
      if (this.product.isAvailable) {
        return 'Available';
      } else {
        return 'Out of Stock';
      }
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
