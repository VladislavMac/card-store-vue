<template>
    <section class="content-products-section">
        <div class="content-products-section-img">
            <img
            :src="product.img"
            alt="product.title"
            >
        </div>
        <div class="content-products-section-title">
            <h1 class="content-products-section-title_title">
                {{ product.title }}
            </h1>
        </div>
        <div class="content-products-section-desc">
            <p class="content-products-section-desc_desc">
                {{ product.desc }}
            </p>
        </div>
        <div class="content-products-section-buttons">
            <div class="content-products-section-buttons-add">
                <button
                @click="$emit('addWantedProduct', product)"
                class="content-products-section-buttons-add_button"
                >
                    В корзину
                </button>
            </div>
            <div class="content-products-section-buttons-price">
                <p class="content-products-section-buttons-price_price">
                    ${{ product.price }}
                </p>
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
            'addWantedProduct'
        ],
        data() {
            return{
            }
        }
    }
</script>
  
<style src="../scss/products/Products.css" scoped></style>