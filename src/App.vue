<template>
    <div id="app">
        <AgeGate v-if="!ageValid" @ageGateComplit="ageComplite" ></AgeGate>
        <swiper-wrap v-else ></swiper-wrap>
    </div>
</template>

<script>
    import AgeGate from "@/components/AgeGate";
    import SwiperWrap from "@/components/SwiperWrap";

    export default {
        name: 'App',
        components: {
            SwiperWrap,
            AgeGate
        },
        data() {
            return {
                ageValid: false,
            }
        },
        methods: {
            ageComplite(){
                this.ageValid = true
            }
        },
    }
</script>

<style>
    #app {
        font-family: 'jj rg';
        color: rgb(239, 222, 161);
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
    }
</style>
