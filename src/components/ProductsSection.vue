<template>
    <section class="content-products-section">
        <div class="content-products-section-img">
            <img
            :src="product.img"
            alt="">
        </div>
        <div class="content-products-section-title">
            <h1 class="content-products-section-title_title">{{ product.name }}</h1>
        </div>
        <div class="content-products-section-desc">
            <p class="content-products-section-desc_desc">
                {{ product.desc }}
            </p>
        </div>
        <div class="content-products-section-buttons">
            <div class="content-products-section-buttons-add">
                <button
                class="content-products-section-buttons-add_button">В корзину</button>
            </div>
            <div class="content-products-section-buttons-counter">
                <button 
                @click="$emit('reduceCount')"
                class="content-products-section-buttons-counter_button">-</button>

                <p class="content-products-section-buttons-counter_out">
                {{ product.count }}
                </p>

                <button 
                @click="$emit('increaseCount')"
                class="content-products-section-buttons-counter_button">+</button>
            </div>
        </div>
    </section>
</template>
  
<script>
    export default {
        name: 'ProductsSection',
        props : {
            product : Object,
        },
        emits : [
            'reduceCount',
            'increaseCount',
        ],
        data() {
            return{
            }
        }
    }
</script>
  
<style src="../scss/products/Products.css" scoped></style>