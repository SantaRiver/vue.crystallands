<template>
    <div class="panel container-fluid container-xl">
        <div class="row">
            <div class="panel__item col-2 d-flex align-self-center position-relative">
                <img class="w-100" v-bind:src="'../../images/interface/health.png'" alt="health">
                <div class="w-100 h-100 position-absolute d-flex justify-content-center align-items-center">
                    <p class="stat mb-0">{{ userStats['health'] }}</p>
                </div>
            </div>
            <div class="panel__item col-2 d-flex align-self-center position-relative">
                <img class="w-100" v-bind:src="'../../images/interface/hunger.png'" alt="hunger">
                <div class="w-100 h-100 position-absolute d-flex justify-content-center align-items-center">
                    <p class="stat mb-0">{{ userStats['hunger'] }}</p>
                </div>
            </div>
            <div class="col-4 position-relative">

                <img class="w-100" v-bind:src="'../../images/interface/wallet-btn.png'" alt="wallet-btn">

            </div>
            <div class="panel__item col-2 d-flex align-self-center position-relative">
                <img class="w-100" v-bind:src="'../../images/interface/energy.png'" alt="energy">
                <div class="w-100 h-100 position-absolute d-flex justify-content-center align-items-center">
                    <p class="stat mb-0">{{ userStats['energy'] }}</p>
                </div>
            </div>
            <div class="panel__item col-2 d-flex align-self-center position-relative">
                <img class="w-100" v-bind:src="'../../images/interface/money.png'" alt="money">
                <div class="w-100 h-100 position-absolute d-flex justify-content-center align-items-center">
                    <p class="stat mb-0">{{ userWallet['balance'] }}</p>
                </div>
            </div>
        </div>
    </div>

</template>

<script>
import {mapGetters} from "vuex";

export default {
    name: "Panel",
    computed: mapGetters(["userStats", "userWallet"]),
}
</script>

<style scoped>

</style>
