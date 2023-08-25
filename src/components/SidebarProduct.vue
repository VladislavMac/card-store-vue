<template>
    <li class="sidebar-content-list_item">
    <div class="sidebar-content-list_item-img">
        <img
        :src=" wantedProduct.img " 
        :alt=" wantedProduct.name "
        class="sidebar-content-list_item-img_img">
    </div>
    <div class="sidebar-content-list_item-title">
        <h1 class="sidebar-content-list_item-title_title">
            {{ wantedProduct.name }}
        </h1>
    </div>
    <div class="sidebar-content-list_item-price">
        <div class="sidebar-content-list_item-price-counter">
            <button 
            @click="$emit('reduceCount')"
            class="sidebar-content-list_item-price-counter_button">
                -
            </button>

            <p class="sidebar-content-list_item-price-counter_out">
                1
            </p>

            <button 
            @click="$emit('increaseCount')"
            class="sidebar-content-list_item-price-counter_button">
                +
            </button>
        </div>
        <div class="sidebar-content-list_item-price-price">
            <p class="sidebar-content-list_item-price-price_p">
                x <span>${{ wantedProduct.money }}</span>
            </p>
        </div>
    </div>
    <div class="sidebar-content-list_item-button">
        <button class="sidebar-content-list_item-button_button">
            x
        </button>
    </div>
    </li>
</template>

<script>

export default {
    props : {
        wantedProduct : Array
    },
}

</script>

<style src="../scss/sidebar/Sidebar.css" scoped></style>