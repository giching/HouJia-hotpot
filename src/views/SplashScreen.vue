<script>
import hotpotAnimation from '@/assets/Animated-Logo.mp4'

export default {
    name: 'SplashScreen',
    mounted() {
        setTimeout(() => {
            this.$router.push('/home');
        }, 7000); // 3秒後跳轉到首頁
    },
    data(){
        return{
            hotpotAnimation,
        }
    }
};
</script>

<template>
    <video ref="videoRef" autoplay muted loop>
        <source :src="hotpotAnimation" type="video/mp4">
    </video>
</template>
<style scoped>
video {
    width: 100%;
    height: 100vh;
    object-fit: cover;
}
</style>
