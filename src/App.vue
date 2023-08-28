<template>
  <app-sidebar
  :wantedProductsPrice="wantedProductsPrice"
  >
    <sidebar-product
      v-for="wantedProduct in wantedProducts"
      
      :key="wantedProduct.id"
      :wantedProduct="wantedProduct"
      @removeWantedProduct="removeWantedProduct(wantedProduct)"
    />
  </app-sidebar>
  <app-header />
  <hr>
  <app-products :products="products">
    <products-section
      v-for="product in products"

      :key="product.id"
      :product="product"

      @addWantedProduct="addWantedProduct(product)"
    />
  </app-products>
</template>

<script>

import AppSidebar from './components/AppSidebar.vue'
import SidebarProduct from './components/SidebarProduct.vue'
import AppHeader from './components/AppHeader.vue'
import AppProducts from './components/AppProducts.vue'
import ProductsSection from './components/ProductsSection.vue'


export default {
  name: 'App',
  components: {
    AppHeader,
    AppProducts,
    AppSidebar,
    ProductsSection,
    SidebarProduct
  },
  methods :{
    removeProduct(product){
      this.wantedProducts.splice(this.wantedProducts.indexOf(this.wantedProducts.filter((wantedProduct) => wantedProduct.id === product.id )[0]), 1)
    },
    removeWantedProduct(product){
      this.removeProduct(product) 
      this.wantedProductsPrice -= product.money
    },
    addWantedProduct(product){
      this.wantedProducts.push(product) 
      this.wantedProductsPrice += product.money
    }
  },
  data() {
    return{
      wantedProducts : [],
      wantedProductsPrice : 0,
      products : [
        {
          id : 0,
          name : 'GeForce RTX 3050',
          img : 'https://ir.ozone.ru/s3/multimedia-f/c1000/6303134703.jpg',
          desc : 'GeForce GTX 1050 2GB GDDR5 128bit (GV-N1050D5-2GD)',
          count : 0,
          money : 2153
        },
        {
          id : 1,
          name : 'GeForce RTX 3090',
          img : 'https://ir.ozone.ru/s3/multimedia-4/c1000/6032580688.jpg',
          desc : 'GeForce GTX 1050 2GB GDDR5 128bit (GV-N1050D5-2GD)',
          count : 0,
          money : 2354
        },
        {
          id : 2,
          name : 'GeForce RTX 3050',
          img : 'https://shop.by/images/msi_geforce_rtx_3050_gaming_x_8g_5.webp',
          desc : 'GeForce GTX 1050 2GB GDDR5 128bit (GV-N1050D5-2GD)',
          count : 0,
          money : 2251
        },
        {
          id : 3,
          name : 'GeForce GTX 1050',
          img : 'https://fotobumaga.by/wp-content/uploads/2020/04/GV-N1050D5-2GD.png',
          desc : 'GeForce GTX 1050 2GB GDDR5 128bit (GV-N1050D5-2GD)',
          count : 0,
          money : 1650
        },
        {
          id : 4,
          name : 'GeForce GTX 960',
          img : 'https://www.hardwareluxx.ru/media/jphoto/news-galerien/asus-geforce-gtx-960-mini-bei-geizhalsat/geizhalst-asus-gtx960mini-01-500x435.png',
          desc : 'GeForce GTX 1050 2GB GDDR5 128bit (GV-N1050D5-2GD)',
          count : 0,
          money : 896
        },
        //
        {
          id : 5,
          name : 'GeForce RTX 3050',
          img : 'https://ir.ozone.ru/s3/multimedia-f/c1000/6303134703.jpg',
          desc : 'GeForce GTX 1050 2GB GDDR5 128bit (GV-N1050D5-2GD)',
          count : 0,
          money : 2153
        },
        {
          id : 6,
          name : 'GeForce RTX 3090',
          img : 'https://ir.ozone.ru/s3/multimedia-4/c1000/6032580688.jpg',
          desc : 'GeForce GTX 1050 2GB GDDR5 128bit (GV-N1050D5-2GD)',
          count : 0,
          money : 2354
        },
        {
          id : 7,
          name : 'GeForce RTX 3050',
          img : 'https://shop.by/images/msi_geforce_rtx_3050_gaming_x_8g_5.webp',
          desc : 'GeForce GTX 1050 2GB GDDR5 128bit (GV-N1050D5-2GD)',
          count : 0,
          money : 2251
        },
        {
          id : 8,
          name : 'GeForce GTX 1050',
          img : 'https://fotobumaga.by/wp-content/uploads/2020/04/GV-N1050D5-2GD.png',
          desc : 'GeForce GTX 1050 2GB GDDR5 128bit (GV-N1050D5-2GD)',
          count : 0,
          money : 1650
        },
        {
          id : 9,
          name : 'GeForce GTX 960',
          img : 'https://www.hardwareluxx.ru/media/jphoto/news-galerien/asus-geforce-gtx-960-mini-bei-geizhalsat/geizhalst-asus-gtx960mini-01-500x435.png',
          desc : 'GeForce GTX 1050 2GB GDDR5 128bit (GV-N1050D5-2GD)',
          count : 0,
          money : 896
        },
      ],
    }
  }
}
</script>

<style src="./scss/app/App.css"></style>

<!-- <template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style> -->
