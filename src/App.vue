<template>
  <div id="app">
    <display></display>
    <product></product>
    <shopping-cart></shopping-cart>
  </div>
</template>
<script>
import Display from './components/Display'
import Product from './components/Product'
import ShoppingCart from './components/ShoppingCart'
export default {
  components:{ Display,Product,ShoppingCart }
}
</script>

<style>
</style>
