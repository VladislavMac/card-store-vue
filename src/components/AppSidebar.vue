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
                <slot></slot>
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
    data(){
        return{
            sidebarWidth : 0,
            sidebarOpen : false
        }
    }
}
</script>

<style src="../scss/sidebar/Sidebar.css" scoped></style>