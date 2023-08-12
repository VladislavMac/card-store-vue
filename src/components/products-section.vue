<template>
    <div class="content-products-section-img">
        <img
        :src="img"
        alt="">
    </div>
    <div class="content-products-section-title">
        <h1 class="content-products-section-title_title">{{ name }}</h1>
    </div>
    <div class="content-products-section-desc">
        <p class="content-products-section-desc_desc">
            {{ desc }}
        </p>
    </div>
    <div class="content-products-section-buttons">
        <div class="content-products-section-buttons-add">
            <button
            class="content-products-section-buttons-add_button">В корзину</button>
        </div>
        <div class="content-products-section-buttons-counter">
            <button 
            class="content-products-section-buttons-counter_button">-</button>

            <p class="content-products-section-buttons-counter_out">
            {{ count }}
            </p>

            <button 
            class="content-products-section-buttons-counter_button">+</button>
        </div>
    </div>
</template>
  
<script>
    export default {
        name: 'products-section',
        props : {
            img   : String,
            desc  : String,
            count : Number,
            money : Number,
        },
        data() {
            return{
            }
        }
    }
</script>
  
<style src="../scss/products/Products.css" scoped></style>