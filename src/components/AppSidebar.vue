<template>
    <div
    :style="{
        width: sidebarWidth + 'vw' 
    }"
    class="sidebar">
        <div class="sidebar-button">
            <button 
            v-if="sidebarOpen"
            @click="
                sidebarOpen = false, 
                sidebarWidth = 0
            "
            class="sidebar-button_button">
                x
            </button>

            <button 
            v-if="!sidebarOpen"
            @click="
                sidebarOpen = true, 
                sidebarWidth = 50
            "
            class="sidebar-button_button">
                +
            </button>
        </div>

        <div class="sidebar-content">
            <ul class="sidebar-content-list">
                <li class="sidebar-content-list_item">
                    <div class="sidebar-content-list_item-img">
                        <img src="../img/960.jpg" alt="" class="sidebar-content-list_item-img_img">
                    </div>
                    <div class="sidebar-content-list_item-title">
                        <h1 class="sidebar-content-list_item-title_title">
                            Geforce GTX 3660
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
                                x <span>$2100</span>
                            </p>
                        </div>
                    </div>
                    <div class="sidebar-content-list_item-button">
                        <button class="sidebar-content-list_item-button_button">
                            x
                        </button>
                    </div>
                </li>
            </ul>
            <hr>
            <div class="sidebar-content-pay">
                <div class="sidebar-content-pay-price">
                    <p class="sidebar-content-pay-price_price">К оплате: <span>$2831</span></p>
                </div>
                <div class="sidebar-content-pay-button">
                    <button class="sidebar-content-pay-button_button">Оформить заказ</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name : 'app-sidebar',
    props : {
        itemsBuy : Array,
    },
    data(){
        return{
            sidebarWidth : 0,
            sidebarOpen : false
        }
    }
}
</script>

<style src="../scss/sidebar/Sidebar.css" scoped></style>