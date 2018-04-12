<template>
  <div>
  <ul>
    <li v-for="product in products">
      {{ product.title }} - {{ product.price | currency}}
      <button
        :disabled="!product.inventory"
        @click="addProductToCart(product)">
        Add to cart
      </button>
    </li>
  </ul>
    <hr>
  </div>
</template>

<script type="text/ecmascript-6">
  import { mapGetters, mapActions } from 'vuex'

  export default {
    // mapGetters将 store 中的 getter 映射到局部计算属性中
    computed: mapGetters({
      products: 'allProducts'
    }),
    methods: mapActions([
      'addProductToCart'
    ]),
    created () {
      this.$store.dispatch('getAllProducts')
    }
  }
</script>

<style>
</style>

