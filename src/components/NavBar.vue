<script>
import logo from '@/assets/houjialogo.png'
import { RouterLink } from 'vue-router'

export default{
    data() {
        return{
            logo,
        }
    },
}
</script>
<template>
    <div class="nav-bar-all">
        <div class="row flex justify-between">
            <!-- Nav Logo -->
            <section class="">
                <div id="nav-img">
                    <a class="" href=""><img class="logo" :src=logo alt="HouJia-logo"></a>
                </div>
            </section>
            <section class="w-full border-4 border-pink-200 text-end">
                <!-- <RouterLink to="/">Contact</RouterLink> -->
                <!-- <RouterLink to="/">News</RouterLink>
                <RouterLink to="about">Menu</RouterLink> -->
                <div class="">
                    <!-- <nav class="navbar navbar-expand-md">
                        <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
                            data-bs-target="#navDropdown">
                            <span class="navbar-toggler-icon"></span>
                        </button>
                        <div class="collapse navbar-collapse" id="navDropdown">
                            <ul class="navbar-nav">
                                <li class="nav-item"><a class="nav-link" href="">News</a></li>
                                <li class="nav-item dropdown">
                                    <a class="nav-link dropdown-toggle" data-bs-toggle="dropdown">Menu</a>
                                    <div class="dropdown-menu">
                                        <a class="dropdown-item" href="">Soup</a>
                                        <a class="dropdown-item" href="">Ingredient</a>
                                        <a class="dropdown-item" href="">Side</a>
                                        <a class="dropdown-item" href="">Drink</a>
                                    </div>
                                </li>
                                <li class="nav-item"><a class="nav-link" href="">Contact</a></li>
                                <li class="nav-item"><a class="nav-link" href="">Reservation</a>
                                </li>
                            </ul>
                        </div>
                    </nav> -->
                </div>
            </section>
        </div>
    </div>
</template>
<style scoped>
.nav-bar-all{
    width: 100%;
    background-color: rgba(255, 199, 135, 0.637);
    padding: 10px;
    backdrop-filter: blur(5px);
}
.row{
    padding: 10px;
    margin: 0;
    /* display: flex; */
}
#nav-img{
    border: 2px solid yellow;
    /* height:50px; */
    width:100%;
}
img{
    height:10vh;
    width: auto;
}
.navbar-nav{
    width: 100%;
    display: flex;
    justify-content: end;
    align-items: center;
    gap: 12px;
}
</style>
