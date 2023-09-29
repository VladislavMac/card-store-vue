<template>
    <li class="sidebar-content-list_item">
        <div class="sidebar-content-list_item-img">
            <img
            :src=" wantedProduct.img " 
            :alt=" wantedProduct.title "
            class="sidebar-content-list_item-img_img"
            >
        </div>
        <div class="sidebar-content-list_item-title">
            <h1 class="sidebar-content-list_item-title_title">
                {{ wantedProduct.title }}
            </h1>
        </div>
        <div class="sidebar-content-list_item-price">
            <div class="sidebar-content-list_item-price-counter">

                <button 
                @click="$emit('increaseCountWantedProduct')"
                class="sidebar-content-list_item-price-counter_button"
                >
                    +
                </button>
                
                <p class="sidebar-content-list_item-price-counter_out">
                    {{ wantedProduct.count }}
                </p>

                <button 
                @click="$emit('reduceCountWantedProduct')"
                class="sidebar-content-list_item-price-counter_button"
                >
                    -
                </button>
            </div>
            <div class="sidebar-content-list_item-price-price">
                <p class="sidebar-content-list_item-price-price_p">
                    x <span>${{ wantedProduct.price }}</span>
                </p>
            </div>
        </div>
        <div class="sidebar-content-list_item-button">
            <button
            @click="$emit('removeWantedProduct', wantedProduct)"
            class="sidebar-content-list_item-button_button"
            >
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
    data(){
        return{
        }
    }
}

</script>

<style src="../scss/sidebar/Sidebar.css" scoped></style>