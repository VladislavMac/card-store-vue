<template>
  <div class="content">
    <div class="content-products">
      <section
      v-for="product in products"
      :key="product.name"
      class="content-products-section">
        <products-section
        :product="product"

        @reduceCount   = "( product.count > 0 ) ? product.count-- : false"
        @increaseCount = "( product.count < 99 ) ? product.count++ : false"
        
        />
      </section>
    </div>
  </div>
</template>


<script>
  import ProductsSection from './products-section.vue'

  export default {
    name: 'app-products',
    components : {
      ProductsSection
    },
    data() {
      return{
        products : [
        {
          name : 'GeForce RTX 3050',
          img : 'https://ir.ozone.ru/s3/multimedia-f/c1000/6303134703.jpg',
          desc : 'GeForce GTX 1050 2GB GDDR5 128bit (GV-N1050D5-2GD)',
          count : 0,
          money : 2153
        },
        {
          name : 'GeForce RTX 3090',
          img : 'https://ir.ozone.ru/s3/multimedia-4/c1000/6032580688.jpg',
          desc : 'GeForce GTX 1050 2GB GDDR5 128bit (GV-N1050D5-2GD)',
          count : 0,
          money : 2354
        },
        {
          name : 'GeForce RTX 3050',
          img : 'https://shop.by/images/msi_geforce_rtx_3050_gaming_x_8g_5.webp',
          desc : 'GeForce GTX 1050 2GB GDDR5 128bit (GV-N1050D5-2GD)',
          count : 0,
          money : 2251
        },
        {
          name : 'GeForce GTX 1050',
          img : 'https://fotobumaga.by/wp-content/uploads/2020/04/GV-N1050D5-2GD.png',
          desc : 'GeForce GTX 1050 2GB GDDR5 128bit (GV-N1050D5-2GD)',
          count : 0,
          money : 1650
        },
        {
          name : 'GeForce GTX 960',
          img : 'https://www.hardwareluxx.ru/media/jphoto/news-galerien/asus-geforce-gtx-960-mini-bei-geizhalsat/geizhalst-asus-gtx960mini-01-500x435.png',
          desc : 'GeForce GTX 1050 2GB GDDR5 128bit (GV-N1050D5-2GD)',
          count : 0,
          money : 896
        },
        //
        {
          name : 'GeForce RTX 3050',
          img : 'https://ir.ozone.ru/s3/multimedia-f/c1000/6303134703.jpg',
          desc : 'GeForce GTX 1050 2GB GDDR5 128bit (GV-N1050D5-2GD)',
          count : 0,
          money : 2153
        },
        {
          name : 'GeForce RTX 3090',
          img : 'https://ir.ozone.ru/s3/multimedia-4/c1000/6032580688.jpg',
          desc : 'GeForce GTX 1050 2GB GDDR5 128bit (GV-N1050D5-2GD)',
          count : 0,
          money : 2354
        },
        {
          name : 'GeForce RTX 3050',
          img : 'https://shop.by/images/msi_geforce_rtx_3050_gaming_x_8g_5.webp',
          desc : 'GeForce GTX 1050 2GB GDDR5 128bit (GV-N1050D5-2GD)',
          count : 0,
          money : 2251
        },
        {
          name : 'GeForce GTX 1050',
          img : 'https://fotobumaga.by/wp-content/uploads/2020/04/GV-N1050D5-2GD.png',
          desc : 'GeForce GTX 1050 2GB GDDR5 128bit (GV-N1050D5-2GD)',
          count : 0,
          money : 1650
        },
        {
          name : 'GeForce GTX 960',
          img : 'https://www.hardwareluxx.ru/media/jphoto/news-galerien/asus-geforce-gtx-960-mini-bei-geizhalsat/geizhalst-asus-gtx960mini-01-500x435.png',
          desc : 'GeForce GTX 1050 2GB GDDR5 128bit (GV-N1050D5-2GD)',
          count : 0,
          money : 896
        },
        //
        ],
      }
    }
  }
  // props: {
  //  msg: String
// }
</script>

<style src="../scss/products/Products.css" scoped></style>