<template>
  <div class="content">
    <div class="content-products">
      <slot></slot>
    </div>
  </div>
</template>

<script>
  // @reduceCount      = "( product.count > 0 )  ? product.count-- : false" 
  // @increaseCount    = "( product.count < 99 ) ? product.count++ : false"
  export default {
    name: 'AppProducts',
    props : {
      products : Array
    },
    data() {
      return{
        
      }
    }
  }
  // props: {
  //  msg: String
// }
</script>

<style src="../scss/products/Products.css" scoped></style>