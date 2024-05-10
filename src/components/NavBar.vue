<script>
import logo from '@/assets/houjialogo.png'
import { RouterLink } from 'vue-router'

export default {
    data() {
        return {
            // img&icon
            logo,

            // variable
            menuSwitch: false,
        }
    },
    methods:{
        // control menuBtn
        menuBtn() {
                this.menuSwitch = !this.menuSwitch;
        },
    },
}
</script>
<template>
    <div class="nav-bar-all absolute top-0 z-30 bg-transparent">
        <div class="row flex justify-between">
            <!-- Nav Logo -->
            <section class="">
                <div id="nav-img">
                    <RouterLink to="home"><img class="logo" :src=logo alt="HouJia-logo"></RouterLink>
                </div>
            </section>
            <section class="w-full text-white text-[24px] flex justify-end relative">
                <!-- <RouterLink to="/">Contact</RouterLink> -->
                <RouterLink to="/" class="link-style">News</RouterLink>
                <button type="button" class="link-style" @click="menuBtn()">Menu v</button>
                <div class=" absolute top-[90px] right-0 dropdown-menu" v-if="menuSwitch === true">
                    <ol class="flex flex-col py-2 gap-2 text-start w-full">
                        <RouterLink to="about" class="dropdown-item">All</RouterLink>
                        <a class="dropdown-item" href="">Soup</a>
                        <a class="dropdown-item" href="">Ingredient</a>
                        <a class="dropdown-item" href="">Side</a>
                        <a class="dropdown-item" href="">Drink</a>
                    </ol>
                </div>
            </section>
        </div>
    </div>
</template>
<style scoped>
.nav-bar-all {
    width: 100%;
    /* background-color: rgba(255, 199, 135, 0.637); */
    padding: 6px 80px;
    /* backdrop-filter: blur(5px); */
}

.link-style {
    display: flex;
    align-items: center;
    padding: 0 40px;
}
.dropdown-menu {
    background-color: #c6c6c665;
    backdrop-filter: blur(5px);
    border-radius: 5px;
}

.dropdown-item {
    padding:8px 20px;
}
.dropdown-item:hover{
    background-color: #9b9b9b65;
    color: rgb(255, 209, 123);
}

.row {
    padding: 10px;
    margin: 0;
    /* display: flex; */
}

#nav-img {
    /* border: 2px solid yellow; */
    /* height:50px; */
    width: 100%;
}

img {
    height: 10vh;
    width: auto;
}

.navbar-nav {
    width: 100%;
    display: flex;
    justify-content: end;
    align-items: center;
    gap: 12px;
}
</style>
